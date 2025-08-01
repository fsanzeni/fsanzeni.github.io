+++
title = 'CH32V Microcontrollers'
date = 2025-07-31T09:18:00+01:00
summary = "Documenting my first foray into programming these low-cost RISC-V microcontrollers from WCH"
showSummary = true
categories = ["Project"]
tags = ["risc-v","CH32V","tutorial"]
+++

# Introduction
I've spoken about open source hw/sw at length these days and I've finally come around at putting together a bit of a project log about WCH's cheap mcus.

In any case, being used to STM32s and their great documentation, I thought I could just "read the docs" and figure out how things would work. Big mistake. 

I'm not fond of blinking LEDs but even that wasn't super easy, as the docs are sparse. But if you drill into the various header files, you get the picture of how to use the GPIOs. Don't worry, you don't have to do it too, [I've compiled a handy-dandy overview of all the functions you can use when using the GPIO]({{< ref "gpio.md" >}}).

## Blink and you'll miss it
Now to brass tacks. Let's blink the LED (in this case using Port B, pin 1 - i.e., PB1):

```c
#include "debug.h"

void led_gpio_init(void) {
    GPIO_InitTypeDef GPIO_InitStructure;

    // Enable GPIOB clock
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);

    // Set PB1 as output push-pull
    GPIO_StructInit(&GPIO_InitStructure);    // Fills with default values
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_2MHz;
    GPIO_Init(GPIOB, &GPIO_InitStructure);  // Initialise PB1 with config
}


int main(void)
{
    SystemCoreClockUpdate();
    Delay_Init();

    led_gpio_init();

    while(1)
    {
        // Turn LED ON
        GPIO_SetBits(GPIOB, GPIO_Pin_1);
        Delay_Us(1000000);

        // Turn LED OFF
        GPIO_ResetBits(GPIOB, GPIO_Pin_1);
        Delay_Us(1000000);
    }
}
```
Now that all seems sensible, doesn't it? But what about that sneaky function, ``SystemCoreClockUpdate()``? [It's described in the ``system_ch32vxxx.h`` and ``system_ch32vxxx.c`` files]({{< ref "system.md" >}}).

Are we done yet? Not so fast. Remember this function from our blinky example?
```c
void led_gpio_init(void) {
    GPIO_InitTypeDef GPIO_InitStructure;

    // Enable GPIOB clock
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);

    // Set PB1 as output push-pull
    GPIO_StructInit(&GPIO_InitStructure);    // Fills with default values
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_2MHz;
    GPIO_Init(GPIOB, &GPIO_InitStructure);  // Initialise PB1 with config
}
```
Do you notice anything I haven't explained yet? What's that `RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);` doing there? [That's part of the Reset and Clock Control functions]().

That's all for now, but I'll keep updating this page as I go forward writing code.
