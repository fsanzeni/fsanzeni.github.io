+++
title = 'CH32Vxxx system.c overview'
url = '/ch32v/system/'
date = 2025-07-31T09:18:00+01:00
summary = "Documentation for the system"
showSummary = true
categories = ["Project"]
tags = ["risc-v","CH32V","tutorial"]
[ build ]
  list = 'local'
  render = true
+++

## system_ch32vxxx.c
The `system.c` file manages the system clock configuration.

- The system clock (SYSCLK) is the main frequency source for the CPU core.
- This clock can be derived from either an internal oscillator (HSI) or an external crystal oscillator (HSE).
- Often, a Phase-Locked Loop (PLL) is used to multiply the base clock frequency to reach higher speeds.
- Proper clock configuration ensures correct peripheral operation and timing accuracy.

### Key Variables and Macros

- `SystemCoreClock`
A global variable holding the current core clock frequency (Hz). It is updated whenever the clock setup changes. Your code and HAL use it for delay calculations and peripheral timing.
- `SYSCLK_FREQ_*` macros
Preprocessor definitions like `SYSCLK_FREQ_96MHz_HSE` select the target clock frequency and source. In your file, only one should be uncommented to choose the system clock configuration.
Example:

```c
#define SYSCLK_FREQ_96MHz_HSE  96000000
```

- `HSI_VALUE`, `HSE_VALUE`
Constants defining the frequency of internal and external oscillators, typically 8 MHz or 32 MHz depending on the chip variant.

### Functions

#### `SystemInit(void)`

- Called early during MCU reset/startup (usually from startup assembly).
- Resets RCC (clock control) registers to a known state.
- Enables the internal oscillator (HSI) as a safe default.
- Calls `SetSysClock()` to configure and switch the system clock based on selected macro.
- Prepares Flash memory interface and bus prescalers suitably.

#### `SystemCoreClockUpdate(void)`

- Reads current clock configuration registers.
- Calculates the active core clock frequency based on oscillator source, PLL multiplier, and bus prescalers.
- Updates the global `SystemCoreClock` variable.
- Useful to call after runtime clock changes to refresh your software’s knowledge of CPU frequency.

#### `SetSysClock(void)` (static helper)

- Dispatches to one of many `SetSysClockTo...()` functions depending on which frequency macro is active.
- Ensures the correct clock setup function is called based on your frequency choice (e.g., `SetSysClockTo96_HSE()`).

#### `SetSysClockToXX_YYY()` functions

- There are many functions like `SetSysClockTo96_HSE()`, `SetSysClockTo72_HSI()` that configure:
    - Enabling and stabilizing the source oscillator (HSI or HSE).
    - Configuring and enabling the PLL with appropriate multipliers.
    - Setting bus prescalers for AHB, APB1, APB2 to safe clocks.
    - Switching SYSCLK source to PLL output.
    - Waiting for clock source switch to complete.
- Each function targets a specific frequency and clock source combination.

### Summary Table

| Function | Purpose | Usage Context |
| :-- | :-- | :-- |
| `SystemInit()` | Initialise system clocks on startup | Called once early in startup |
| `SystemCoreClockUpdate()` | Update global clock frequency variable | Called after clock config changes |
| `SetSysClock()` | Select and call appropriate clock setup | Internal helper function |
| `SetSysClockToXX_YYY()` | Configure specific frequency and source | Called by `SetSysClock` based on user choice |

### Practical Notes

- Only one `SYSCLK_FREQ_*` macro should be active at a time.
- If your board has an external crystal (HSE), prefer using it for better accuracy.
- PLL allows running at higher clock rates derived from base oscillators.
- Bus prescalers ensure peripherals run safely within their speed limits.
- If no macro is selected, MCU defaults to using the internal oscillator (HSI).
- Use `SystemCoreClock` variable in your code for timing functions.
- Call `SystemCoreClockUpdate()` if you change clock settings at runtime.

### Example Usage

At the very start of your program or in startup code, `SystemInit()` is invoked to configure your desired system clock frequency. Later, if clock settings change, `SystemCoreClockUpdate()` can be called to keep track of current CPU speed.

```c
int main(void) {
    SystemInit();
    // Your application code here

    while(1){
        // Application loop
    }
}
```