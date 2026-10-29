# 예제 01 · 누클레오 첫 굽기 — LED 깜빡이기

설명: https://smilebeen.github.io/examples/ex01/

## 만드는 법
1. CubeMX → Board Selector → `NUCLEO-G474RE` → 기본값으로 초기화 **Yes**
2. Project Manager: 이름 `ex01-blink`, Toolchain **STM32CubeIDE**, 위치는 **이 레포 폴더** → Generate Code
   (이 README가 있는 폴더 안에 프로젝트 파일이 생겨요)
3. `Core/Src/main.c` 의 `/* USER CODE BEGIN 3 */` 아래:

```c
HAL_GPIO_TogglePin(LD2_GPIO_Port, LD2_Pin);
HAL_Delay(500);
```

4. Build → Debug As → STM32 C/C++ Application → Resume(F8)

## 확인
- LD2(초록)가 0.5초마다 깜빡임
- `HAL_GPIO_TogglePin` 줄에 중단점 → F8마다 한 번씩 바뀜
