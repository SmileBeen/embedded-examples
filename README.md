# embedded-examples

보드 하나로 30분 안에 끝나는 짧은 STM32 실습 모음이에요.
설명과 영상은 허브 사이트 **예제** 메뉴에 있어요 → https://smilebeen.github.io/examples/

| 번호 | 폴더 | 내용 | 보드 |
|---|---|---|---|
| 01 | [ex01-blink](ex01-blink/) | 첫 굽기 · LED 깜빡이기 · 디버거로 멈춰 보기 | NUCLEO-G474RE |
| 02 | [ex02-uart-printf](ex02-uart-printf/) | 가상 COM 포트로 printf · 글자 에코 | NUCLEO-G474RE |

## 쓰는 법
- 도구: STM32CubeMX + STM32CubeIDE 2.x
- 폴더 하나 = CubeIDE 프로젝트 하나. CubeIDE에서 **File → Import → Existing Projects into Workspace**로 폴더를 열어요.
- 직접 쓴 코드는 모두 `/* USER CODE BEGIN */` ~ `END` 사이에 있어요.

## 라이선스
MIT
