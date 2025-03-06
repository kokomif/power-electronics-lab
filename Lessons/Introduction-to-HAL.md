## What is HAL?

HAL (Hardware Abstraction Layer) is a **software library** provided by STMicroelectronics to simplify programming for STM32 microcontrollers. It acts as a "bridge" between your code and the hardware, allowing you to control peripherals (e.g., GPIO, UART, ADC) **without needing to write low-level register operations**.

## Why Use HAL?

1. **Portability**: Code written with HAL can be reused across different STM32 models.
2. **Simplified Coding**: Focus on what your program should do, not how to configure hardware.
3. **Faster Development**: Pre-built functions (e.g., `HAL_GPIO_WritePin()`, `HAL_UART_Transmit()`) speed up prototyping.
4. **Compatibility**: Works seamlessly with STM32CubeMX, a tool for auto-generating code.

## How HAL Works

1. **Abstraction**: HAL hides complex hardware details behind easy-to-use functions.
    - Example: To turn on an LED, call `HAL_GPIO_WritePin(GPIOA, GPIO_PIN_3, GPIO_PIN_SET);` instead of manipulating registers.
2. **Initialization**: HAL handles setup for clocks, peripherals, and interrupts.
3. **Callbacks**: Customize behavior using predefined functions (e.g., `HAL_UART_RxCpltCallback()`).

## Example HAL

* In Arduino:
    ```arduino
    digitalWrite(3, HIGH);
    ```

* In STM32:
    ```c
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_3, GPIO_PIN_SET);
    ```
