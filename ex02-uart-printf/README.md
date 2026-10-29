# 예제 02 · UART로 PC에 글자 보내기 — printf 연결

설명: https://smilebeen.github.io/examples/ex02/

## 만드는 법
1. CubeMX → `NUCLEO-G474RE` → 기본값 **Yes** → 이름 `ex02-uart-printf`
2. Connectivity → **LPUART1** (PA2 · PA3, ST-LINK 가상 COM 포트) : 115200 / 8N1
3. `main.c`

```c
/* USER CODE BEGIN Includes */
#include <stdio.h>

/* USER CODE BEGIN 0 */
int __io_putchar(int ch)
{
  HAL_UART_Transmit(&hlpuart1, (uint8_t *)&ch, 1, HAL_MAX_DELAY);
  return ch;
}

/* USER CODE BEGIN 3 */
uint8_t c;
if (HAL_UART_Receive(&hlpuart1, &c, 1, 1000) == HAL_OK) {
  printf("받음: %c\r\n", c);
} else {
  printf("tick %lu\r\n", HAL_GetTick());
}
```

## 확인
- Tera Term → Serial → `STLink Virtual COM Port (COMx)` → 115200
- 1초마다 `tick ...`, 키를 누르면 `받음: a`
