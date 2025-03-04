# 基于高云 FPGA 的秒表硬件项目说明

## 一、项目概述

本项目使用高云 GW1N-UV9EQ144C6/I5 作为核心板，设计并实现了一款具备计时、暂停 / 恢复、预置时间等功能的秒表。通过本项目，旨在提升数字逻辑设计能力，加深对 FPGA 应用的理解。

## 二、硬件功能

1. **计时功能**：能连续计时 1 小时，从 00:00 到 59:59 后自动重置为 00:00。
2. **显示功能**：利用 7 段 LED 数码管实时显示当前计时。
3. **初始化与预置设置**：可将计时器初值设为 00:00，或预置分秒的任意时间值，如 15:45。
4. **暂停与恢复**：在任意时刻暂停计时，并随时恢复，显示暂停时的计数值。
5. **状态指示**：通过发光二极管（LED）指示秒表的运行、暂停等工作状态。

## 三、硬件设计

1. **核心板**：选用高云 GW1N-UV9EQ144C6/I5 FPGA，其丰富的逻辑资源和高速处理能力满足项目需求。
2. **显示模块**：采用 7 段 LED 数码管，高亮度且易于驱动，直观显示时间。
3. **控制模块**：使用拨码开关和按键实现用户交互，如控制计时、设置时间等。
4. **状态指示模块**：通过 LED 灯的亮灭指示秒表状态。
5. **PCB 设计**：采用 10cm×10cm 双面板，精心绘制 SCH 原理图并进行 PCB 布局，合理走线、添加泪滴并检测，确保电路稳定可靠。

## 四、硬件实现

1. **焊接准备**：预热电烙铁，准备合适焊锡。
2. **焊接过程**：按从低到高顺序焊接，注意 7 段数码管、三极管和 LED 灯的焊接方向，7 段数码管插入焊好的插座以便更换维护。
3. **调试与测试**：完成焊接后进行功能测试，确保各硬件模块正常工作。

## 五、注意事项

1. 电路板使用时轻拿轻放，避免用手触碰芯片引脚，防止静电损坏。
2. 对内部 Flash 下载 bitstream 文件时，确保 MODE 脚状态配置正确。
3. 连接模块时先断电，保障操作安全。
