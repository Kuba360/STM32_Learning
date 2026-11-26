# GPIO on Registers 

## Task
Control LED (`PA5`) and read button (`PC13`) using GPIO registers on STM32.

## Activities
- **Docs:** Read RM0316 sections on RCC (`AHBENR`) and GPIO (`MODER`, `OTYPER`, `ODR`, `BSRR`, `IDR`).
- **Code:** Enable GPIO clocks, blink LED on `PA5` (check loop timing with optimization), and toggle LED with button `PC13`.
- **BSRR note:** `BSRR` is better than `ODR |=` because it executes atomically (no read-modify-write).