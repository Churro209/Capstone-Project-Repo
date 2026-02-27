# Lab Entry – 2026-01-25

## Metadata
- Date: 2026-01-25
- Project:
- Board / Rev:
- Scope: Research Gate Drive IC and generating pwm using Pico C sdk. 

## Objective
learn how the Gate Drive Chip IC works and how to create adjustable pwm on Raspberry pi Pico. 
Read data sheet for the Mosfet we wish to control. 


## Observations
Gate Drive IC Data sheet: [IR2101PBF](https://rocelec.widen.net/view/pdf/l0ksvgwrdh/IRSDS17613-1.pdf?t.download=true&u=5oefqw)

Raspberry Pi Pico C SKD for PWM: [Pico C SDK](https://pip-assets.raspberrypi.com/categories/609-microcontroller-boards/documents/RP-009085-KB-1-raspberry-pi-pico-c-sdk.pdf?disposition=inline)
Pico Example adjusting duty cycle for LED with an interupt: [PWM_IRQ_DutyAdjust_example](https://github.com/raspberrypi/pico-examples/blob/master/pwm/led_fade/pwm_led_fade.c)

mosfet we want to drive data sheet: [IRF3205PBF](https://www.infineon.com/assets/row/public/documents/24/49/infineon-irf3205-datasheet-en.pdf?fileId=5546d462533600a4015355def244190a)
## Conclusions / Next Steps
- The gate drive circuit must have enough voltage to supply the gate such that Vgs >= 4V. 
- The PWM example above is almost exactly what I need, instead of adjusting the duty cycle by the square of the value, I simply need to define a step size to use with feed back. 
- Build the gate drive circuit and start working on the pwm output for week 4. Use multimeter to test pwm and gate drive. 