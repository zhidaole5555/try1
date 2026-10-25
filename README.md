# rask_1

STM32 单片机练习工程。使用 STM32CubeMX 生成初始化代码,Keil MDK(ARM Compiler 6)编译。

## 目录结构

| 路径 | 说明 |
|---|---|
| `Core/` | 应用代码与外设初始化(`main.c`、`stm32f1xx_it.c` 等) |
| `Drivers/` | STM32F1xx HAL 驱动与 CMSIS 库 |
| `MDK-ARM/` | Keil 工程文件,入口为 `rask_1.uvprojx` |
| `rask_1.ioc` | CubeMX 工程配置,修改外设时编辑此文件 |

## 编译

用 Keil µVision 打开 `MDK-ARM/rask_1.uvprojx`,`F7` 编译,`F8` 下载到开发板。

## 版本管理说明

- 编译产物(`*.o`、`*.d`、`*.axf`、`*.hex`、`*.map`、`*.lnp` 等)已由 `.gitignore` 排除,不纳入版本库
- 换行符规则由 `.gitattributes` 统一:源码用 LF,`.bat`、`.ps1`、`.uvprojx` 等 Windows 文件用 CRLF,二进制文件禁止任何转换
- 若在 CubeMX 中修改了工程名,需同步更新 `.gitignore` 里的输出目录路径

## 提交历史

- `673dcee` 练习LED
