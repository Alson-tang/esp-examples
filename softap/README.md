# SOFTAP

- [中文版](#介绍)

## Introduction

This is a simple SoftAP demo demonstrated with ESP32-C3. The following two questions are answered mainly in the form of code：

1. When ESP32-C3 is used as SoftAP, the default IP address is 192.168.4.1. How to modify the default IP address?
2. When ESP32-C3 is used as SoftAP, after a Station is connected, how to obtain the IP address assigned by SoftAP to this Station?

## How to use example

### Configure the project

1. Get Started with ESP-IDF

   Please refer to https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/get-started/index.html for setting up ESP-IDF

2. Set the target chip

   ```
   idf.py set-target esp32c3
   ```

3. Configure the project

   Execute the following command to open the project configuration menu

   ```
   idf.py menuconfig
   ```

   In the `SoftAP Configuration` menu:

   * Set the Wi-Fi configuration.
     * Set `WiFi SSID`.
     * Set `WiFi Password`.
     * Set `WiFi Channel`.
     * Set `Maximal STA connections`.
     * Set `SoftAP ip address`.
     * Set `SoftAP netmask address`.
     * Set `SoftAP gateway address`.

### Build and Flash

Execute the following command to build, flash and monitor the project.

```
idf.py -p PORT flash monitor
```

### Example Output

There is the console output for this example:

```
I (400) phy_init: phy_version 912,d001756,Jun  2 2022,16:28:07
I (450) softap: wifi_init_softap finished. SSID:Alson password:12345678 channel:6
I (75510) softap: station 6a:a8:f3:b3:07:0c join, AID=1
I (76190) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.3
I (76190) softap: the IP address assigned by the SoftAP is192.168.4.3
```

## License

This document and the attached source code are released as Free Software under Apache License Version 2 or later. See the accompanying LICENSE file for a copy.

## 介绍

这是一个使用 ESP32-C3 演示的简单 SoftAP 示例。 主要以代码的形式回答了以下两个问题：

1. ESP32-C3 作为 SoftAP 时，默认的 IP 地址为 192.168.4.1，如何修改默认的 IP 地址？
2. ESP32-C3 作为 SoftAP 时，有 Station 连接上了之后，如何获取 SoftAP 分配给这个 Station 的 IP 地址？

## 如何使用这个示例

### 配置工程

1. 开始使用 ESP-IDF

   ESP-IDF 设置请参考 https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32c3/get-started/index.html

2. 设置目标芯片

   ```
   idf.py set-target esp32c3
   ```

3. 配置工程

   执行以下命令打开项目配置菜单

   ```
   idf.py menuconfig
   ```

   在 `SoftAP Configuration` 菜单中：

   * 设置 Wi-Fi 配置
     * 设置 `WiFi SSID`
     * 设置 `WiFi Password`
     * 设置 `WiFi Channel`
     * 设置 `Maximal STA connections`
     * 设置 `SoftAP ip address`
     * 设置 `SoftAP netmask address`
     * 设置 `SoftAP gateway address`

### 编译和烧录

执行以下命令来编译，烧录和监视工程

```
idf.py -p PORT flash monitor
```

### 示例输出

此示例由控制台输出：

```
I (400) phy_init: phy_version 912,d001756,Jun  2 2022,16:28:07
I (450) softap: wifi_init_softap finished. SSID:Alson password:12345678 channel:6
I (75510) softap: station 6a:a8:f3:b3:07:0c join, AID=1
I (76190) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.3
I (76190) softap: the IP address assigned by the SoftAP is192.168.4.3
```

## 许可证

本文档和随附的源代码在 Apache 许可证版本 2 或更高版本下作为自由软件发布。 请参阅随附的 LICENSE 文件以获取副本。
