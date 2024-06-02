---
title: USB Type-C介绍
C_time: 2024-03-24-16:38
draft: false
tags:
  - #Type-C
  - #PD
  - #USB-IF
  - #USB
---
 
# 介绍

The USB-IF has secured the ubiquitous nature of USB for years to come with the radically updated USB Type-C™ connector. While the sleek new reversible form factor has been significant for generating buzz and excitement from the general consumer market, the significantly expanded feature-set is what will eventually transform the desktop and entertainment environment.

> USB-IF 通过彻底更新的 USB Type-C™ 连接器确保了 USB 的无处不在。虽然时尚的新型可逆外形对于在一般消费市场引起轰动和兴奋具有重要意义，但显着扩展的功能集最终将改变桌面和娱乐环境。

The USB Type-C cable is now poised to become the “universal” cable, as it is capable of supplying blazing fast data transfer speeds of up to 10Gb/s, 100W of continuous power flow, and ultra high bandwidth video capabilities made available through Alternate Modes all in parallel with a single connection.

> USB Type-C 电缆现在有望成为“通用”电缆，因为它能够提供高达 10Gb/s 的超快数据传输速度、100W 的连续功率流以及通过备用模式提供的超高带宽视频功能，所有这些都通过单个连接并行提供。

This document is intended for those already familiar with USB2.0/USB3.0/USB3.1 who are interested in the high level details of the expanded feature set that the USB Type-C cable brings to USB.

> 本文档适用于已经熟悉 USB2.0/USB3.0/USB3.1 的用户，他们对 USB Type-C 电缆为 USB 带来的扩展功能集的高级细节感兴趣。

## 参考文献

This document is an introduction to USB Type-C™ and is not intended to be a replacement to the official specification. Consult the following specifications for technical details not described in this document.

> 本文档是对 USB Type-C™ 的介绍，并非旨在替代官方规范。有关本文档中未描述的技术详细信息，请参阅以下规格。

- USB Type-C™ Specification
- USB Power Delivery 2.0 Specification
- USB 2.0 Specification
- USB 3.0 Specification
- USB 3.1 Specification
- USB Battery Charging BC1.2


# 1 一般信息

The USB Type-C™ cable is a reversible 24-pin interconnect created by the USB-IF. The USB Type-C™ specification was first released in August 2014.

> USB Type-C™ 电缆是由 USB-IF 创建的可逆 24 针互连。USB Type-C™ 规范于 2014 年 8 月首次发布。

The USB Type-C cable is a universal cable that addresses the needs for a wide range of computing, display, and charging applications. The long-term objective of the USB Type-C cable is to replace all previous iterations of the USB cable while greatly expanding the overall capabilities. The recent introduction of the USB Power Delivery and Alternate Mode capabilities further expand the raw potential for even greater adoption of the USB standard in a wider range of applications.

> USB Type-C 电缆是一种通用电缆，可满足各种计算、显示和充电应用的需求。USB Type-C 电缆的长期目标是取代之前所有迭代的 USB 电缆，同时大大扩展整体功能。最近推出的 USB 供电和交替模式功能进一步扩展了 USB 标准在更广泛的应用中采用的原始潜力。

![[Pasted image 20240602151128.png]]

## 1.1 端口行为

Prior to the introduction of USB Type-C™ and USB Power Delivery, data and power roles were typically fixed. The shape of the receptacle/plug dictated both its data role and power role. USB Type-C connections are much more flexible; ports may be host-mode only, device-mode only, or dual-role and both the data and power roles can be independently and dynamically swapped using USB Power Delivery protocol. Because of this, there is some new terminology that is used to describe USB Type-C systems.

> 在引入 USB Type-C™ 和 USB Power Delivery 之前，数据和电源角色通常是固定的。插座/插头的形状决定了其数据角色和电源角色。USB Type-C 连接更加灵活;端口可以是仅主机模式、仅设备模式或双重角色，并且可以使用 USB 供电协议独立动态交换数据和电源角色。因此，有一些新术语用于描述 USB Type-C 系统。

- Downstream Facing Port (DFP) - A host or downstream hub port. Typical of a legacy standard Type-A port.
- Upstream Facing Port (UFP) - A device or upstream hub port. Typical of a legacy standard Type-B port.
- Dual-Role Port (DRP) - A port that transitions between DFP and UFP port states until an attach event occurs.

> • 面向下游的端口（DFP） - 主机或下游集线器端口。传统标准 Type-A 端口的典型特征。
> • 上行端口（UFP） - 设备或上游集线器端口。传统标准 Type-B 端口的典型特征。
> • 双角色端口（DRP） - 在DFP和UFP端口状态之间转换的端口，直到发生连接事件。

DRPs may be dynamically swapped using USB Power Delivery Protocol Negotiation after an initial attach event.
- Power Source or Provider - A source of 5V-20V up to 5A. Typical of a legacy standard Type-A port.
- Power Sink or Consumer - A sink of 5V-20V up to 5A. Typical of a legacy standard Type-B port.

> DRP 可以在初始附加事件后使用 USB 电力传输协议协商动态交换。
> - 电源或提供者 - 5V-20V 高达 5A 的电源源。典型的传统标准 Type-A 端口。
> - 功率接收器或消耗器 - 5V-20V 高达 5A 的接收器。典型的传统标准 Type-B 端口。

## 1.2 Features（功能）

### 1.2.1 MINIMUM FEATURE SET（最小功能集）

A basic USB Type-C application can still be cost-effective.USB Type-C ports are not required to implement all of the advanced features that are defined in the specification. The minimum required feature set includes the following:
- USB2.0 Connection
- Cable attach and detach detection
- VCONN active cable supply

> 基本的 USB Type-C 应用程序仍然具有成本效益。USB Type-C 端口不需要实现规范中定义的所有高级功能。所需的最小功能集包括：
> 	- USB2.0 接口
> 	- 电缆连接和分离检测
> 	- VCONN 有源电缆供应

### 1.2.2 BATTERY CHARGING（电池充电）

While BC1.2 is still supported over USB Type-C because it depends on the USB2.0 lane, a significantly simplified and higher power current capability mechanism is also implemented. This simplified approach involves resistor pull-down/pull-up relationships. These pull-down/pull-up resistors are connected to the CC wire and the upstream facing port (UFP) must monitor the voltage on the CC1 and CC2 pins in order to detect the current sourcing capability of the downstream facing port (DFP) it is connected to. This is a substantial improvement over the complicated handshake mechanisms involved with USB BC1.2.

> 虽然 BC1.2 仍然通过 USB Type-C 受支持，因为它依赖于 USB2.0 通道，但也实现了一种显着简化和更高功率电流能力的机制。这种简化的方法涉及电阻下拉/上拉关系。这些下拉/上拉电阻器连接到 CC 线，上游端口 （UFP） 必须监控 CC1 和 CC2 引脚上的电压，以检测其所连接的下游端口 （DFP） 的电流源能力。这是对 USB BC1.2 所涉及的复杂握手机制的重大改进。

The basic USB Type-C current capabilities are Default USB (500mA for USB2.0 and 900mA for USB3.0), 1.5A@5V, and 3A@5V.
For additional details see Section 3.0, CC Pins.

> 基本的 USB Type-C 电流功能包括默认 USB（USB2.0 为 500mA，USB3.0 为 900mA）、1.5A@5V 和 3A@5V。
> 有关更多详细信息，请参见部分 3.0， CC 引脚。

### 1.2.3 USB2.0, USB3.0, USB3.1, AND BEYOND

The USB Type-C cable is designed to support current generation USB2.0 (480 Mb/s), USB3.0 (5Gb/s), USB3.1 (10Gb/s), and future USB specifications reaching up to 20Gb/s data rates.
For additional details see please refer to the individual specifications as published by the USB-IF.

> USB Type-C 电缆旨在支持当前一代 USB2.0 （480 Mb/s）、USB3.0 （5Gb/s）、USB3.1 （10Gb/s） 以及未来高达 20Gb/s 数据速率的 USB 规格。
> 有关更多详细信息，请参阅 USB-IF 发布的各个规格。

### 1.2.4 POWER DELIVERY 2.0

USB Power Delivery protocol is a singled-ended, 1-wire protocol created by the USB-IF which specifies the methods for serial communication over the USB Type-C CC wire. USB Power Delivery is required for implementation of the following advanced features:

- Communicating with an electronically marked/active cable
- Elevating the VBUS voltage above 5.5V
- Increasing current sourcing/sinking above 3A
- Changing default power roles (Provider or Consumer)
- Using Alternate Modes (see section 1.2.5)

> USB Power Delivery 协议是由 USB-IF 创建的单端 1 线协议，它指定了通过 USB Type-C CC 线进行串行通信的方法。实现以下高级功能需要 USB Power Delivery：
> 	- 使用带有电子标记/有源电缆的电缆进行通信
> 	- 将VBUS电压提升至5.5V以上
> 	- 将电流拉出/灌电流提高到 3A 以上
> 	- 更改默认电源角色（提供者或使用者）
> 	- 使用备用模式（参见第 1.2.5 节）

The Power Delivery 2.0 is a port-to-port and port-to-cable communication protocol. The communication can not propagate throughout an entire device tree like standard USB protocols.
For additional details see Section 5.0, USB Power Delivery 2.0.

> Power Delivery 2.0 是一种端口到端口和端口到电缆的通信协议。通信不能像标准 USB 协议那样在整个设备树中传播。
> 有关更多详细信息，请参见部分 5.0， USB Power Delivery 2.0。

### 1.2.5 ALTERNATE MODES (THIRD PARTY PROTOCOLS)

The USB Type-C cable allows for any third party protocol to be used as long as the cable can support it. Alternate Modes are negotiated and entered on a port-to-port basis using the USB Power Delivery protocol. The following signals may be reassigned when entering an Alternate Mode.
- TX1+/-
- RX1+/-
- TX2+/-
- RX2+/-
- SBU1/SBU2

> USB Type-C 电缆允许使用任何第三方协议，只要电缆可以支持它。备用模式是使用 USB 供电协议在端口到端口的基础上协商和输入的。进入备用模式时，可能会重新分配以下信号。
> 	- TX1+/-
> 	- RX1+/-
> 	- TX2+/-
> 	- RX2+/-
> 	- SBU1/SBU2

Separate specifications define the rules for each Alternate Mode. Currently, specifications exist for DisplayPort (authored by VESA) and ThunderBolt (authored by Intel). For additional details see Section 6.0, Alternate Modes.

> 单独的规范定义了每种备用模式的规则。目前，存在 DisplayPort（由 VESA 编写）和 ThunderBolt（由 Intel 编写）的规范。有关其他详细信息，请参见部分 6.0， 备用模式。

## 1.3 Connector/Receptacle Pins

![[Pasted image 20240602151353.png]]

![[Pasted image 20240602151413.png]]

The USB Type-C connector has 24 pins. Because of its reversibility, the pins are arranged in a mirrored configuration.
There are a total of 6 differential pairs in a full-featured cable assembly. There are also 4 pins that serve functions new to USB: CC1, CC2, SBU1, SBU2.

> USB Type-C 连接器有 24 个针脚。由于其可逆性，引脚以镜像配置排列。
> 一个全功能电缆组件中共有 6 个差分对。还有 4 个引脚用于 USB 的新功能：CC1、CC2、SBU1、SBU2。

### 1.3.1 USB 2.0差分信号对

The 2 sets of USB2.0 differential pairs in the connector pinout only connect to a single differential pair in standard USB2.0 or Full Featured USB Type-C cables. In a typical design, the D+ and D- pins are simply shorted on the PCB so that a multiplexer or switch is not required.

> 连接器引脚排列中的 2 组 USB2.0 差分对仅连接到标准 USB2.0 或全功能 USB Type-C 电缆中的单个差分对。在典型设计中，D+和D-引脚只需在PCB上短路，因此不需要多路复用器或开关。

The second set of pins (B6/B7) may only be re-purposed in docking type applications where only 1 orientation is possible.

> 第二组引脚 （B6/B7） 只能在只能有 1 个方向的对接型应用中重新使用。

### 1.3.2 USB 3.1差分信号对

By default, only one set of TX/RX differential pairs are used for USB3.0/USB3.1 communication, depending on cable insertion orientation. Because of the cable reversibility, the USB3.0/USB3.1 lanes must be rerouted upon orientation connection. A typical application may use a 2:1 multiplexer to achieve this.
USB Power Delivery protocol and Alternate Modes allow some or all of the TX/RX differential pairs to be reassigned.

> 默认情况下，USB3.0/USB3.1 通信仅使用一组 TX/RX 差分对，具体取决于电缆插入方向。由于电缆的可逆性，USB3.0/USB3.1 通道必须在定向连接时重新布线。典型应用可能使用 2：1 多路复用器来实现这一点。
> USB 供电协议和备用模式允许重新分配部分或全部 TX/RX 差分对。

### 1.3.3 CC1/CC2 PINS

The CC1 and CC2 pins are used to connect to the either the CC or VCONN wire in a USB Type-C cable. Both CC1 and CC2 pins must be able to support both CC and VCONN functions. The function is detected upon cable insertion.

> CC1 和 CC2 引脚用于连接到 USB Type-C 电缆中的 CC 或 VCONN 线。CC1 和 CC2 引脚必须能够同时支持 CC 和 VCONN 功能。插入电缆时检测到该功能。

The CC wire is used to cable orientation detection, USB Type-C current capability advertisement and detection, and USB2.0 BMC communication. See Section 3.0, CC Pins for additional details.

> CC 线用于电缆方向检测、USB Type-C 电流能力通告和检测以及 USB2.0 BMC 通信。有关更多详细信息，请参见部分 3.0， CC 引脚。

The VCONN wire is used to power active or electronically marked cables. See Section 4.0, VCONN Supply for additional details.

> VCONN 线用于为有源或E-Marked 电缆供电。有关更多详细信息，请参见部分 4.0， VCONN 电源。

### 1.3.4 SBU1/SBU2

The SBU wires are lower speed signal wires that is allocated for Alternate Mode use only. USB Power Delivery is required for Alternate Mode negotiation before these pins may be used for any purpose.

> SBU 线是仅分配给交替模式使用的低速信号线。在将这些引脚用于任何目的之前，备用模式协商需要 USB Power Delivery。

![[Pasted image 20240602151425.png]]

## 1.4 电源选项

The USB Type-C Interconnect introduces two new native charging options, but is also compatible with legacy charging options. USB Power Delivery is also supported but optional.

> USB Type-C 互连引入了两个新的本机充电选项，但也与传统充电选项兼容。USB Power Delivery 也受支持，但可选。

![[Pasted image 20240602151439.png]]

# 2 USB TYPE-C CABLES

## 2.1 物理规格

### 2.1.1 尺寸

The USB Type-C receptacle opening is 8.34mm x 2.56mm. For comparison, the Type-A receptacle opening is 12.50mm x 5.12mm while the USB3.0 micro-AB receptacle opening is 12.25mm x 1.85mm

> USB Type-C插座开口为8.34mm x 2.56mm。相比之下，Type-A插座开口为12.50mm x 5.12mm，而USB3.0 micro-AB插座开口为12.25mm x 1.85mm

### 2.1.2 耐用性

The USB Type-C cable must minimally support 10,000 mating cycles.

> USB Type-C电缆必须至少支持10,000个配合周期。

### 2.1.3 线缆规格

Signal wire gauge is not explicitly specified in the USB Type-C™ specifications, but wires must be appropriately sized for the length and capabilities of the cable such that:
- Signal integrity on the USB2.0 and USB3.0 wires is preserved
- ~50Ω impedance on the CC and SBU1/SBU2 wires
- Maximum IR drop of 250mV on GND return
- Maximum IR drop of 500mV on VBUS

> USB Type-C™ 规范中未明确规定信号线规，但电线的尺寸必须与电缆的长度和功能相适应，以便：
> 	- 保留 USB2.0 和 USB3.0 线上的信号完整性
> 	- CC 和 SBU1/SBU2 线上的阻抗为 ~50Ω
> 	- GND 返回时最大 IR 压降为 250mV
> 	- VBUS 上的最大 IR 压降为 500mV

### 2.1.4 电缆长度

Cable lengths are not explicitly specified in the USB Type-C™ specifications. However, the electrical requirements create some practical limits. USB3.1 Type-C to Type-C cable assemblies are allocated -6 dB loss at 5GHz, effectively limiting cable lengths to 1 meter. USB3.0 Type-C to Type-C cable assembly are allocated -7 dB loss at 5GHz, effectively limiting cable lengths to 2 meters.

> USB Type-C™ 规范中未明确指定电缆长度。但是，电气要求会产生一些实际限制。USB3.1 Type-C 转 Type-C 电缆组件在 5GHz 时分配了 -6 dB 损耗，有效地将电缆长度限制在 1 米以内。USB3.0 Type-C 转 Type-C 电缆组件在 5GHz 时分配了 -7 dB 损耗，有效地将电缆长度限制在 2 米以内。

![[Pasted image 20240602151450.png]]

## 2.2 USB2.0

A standard USB2.0 Type-C cable assembly is shown in Figure 4 and Table 4.

> 标准USB2.0 Type-C电缆组件如图4和表4所示。

![[Pasted image 20240602151459.png]]

![[Pasted image 20240602151508.png]]

## 2.3 全功能

A standard full-featured USB Type-C cable assembly is shown in Figure 5 and Table 5.

> 标准的全功能USB Type-C电缆组件如图5和表5所示。

![[Pasted image 20240602151516.png]]

![[Pasted image 20240602151521.png]]

## 2.4 被动线缆

A passive USB Type-C cable does not have embedded powered electronics. All passive cables must minimally support USB2.0, and it can support USB Power Delivery up to 60W of power.

> 无源USB Type-C电缆没有嵌入式供电电子设备。所有无源电缆必须最低限度地支持USB2.0，并且可以支持高达60W功率的USB Power Delivery。

## 2.5 有源线缆: E-Marker

An electronically marked cable has embedded electronics that can communicate with the USB ports via USB Power Delivery 2.0 BMC protocol. An electronically marked cable may be powered from the VCONN supply or directly from VBUS and may draw up to 70mW of total power.

> 带有电子标记的电缆具有嵌入式电子设备，可以通过 USB Power Delivery 2.0 BMC 协议与 USB 端口进行通信。带有电子标记的电缆可由 VCONN 电源供电或直接从 VBUS 供电，并可消耗高达 70mW 的总功率。

Use-case Example 1: All USB3.1 compatible USB Type-C cables must be electronically marked.

Use-case Example 2: A 100W Power Delivery cable. Any cable capable of exceeding 60W of power carrying capability must be electronically marked and communicate is capabilities to the DFP port.

> 用例示例 1：所有兼容 USB3.1 的 USB Type-C 电缆都必须进行电子标记。
> 
> 用例示例 2：100W 供电电缆。任何能够超过 60W 功率承载能力的电缆都必须进行电子标记，并与 DFP 端口通信。

An electronically marked cable will behave identically to a standard passive cable if inserted into a receptacle that does not support USB Power Delivery 2.0.

> 如果将带有电子标记的电缆插入不支持 USB Power Delivery 2.0 的插座，其行为将与标准无源电缆相同。

## 2.6 有源线缆: Managed Active Cable

A managed active cable is an electronically marked cable that also has powered USB data reconditioning circuitry. A managed active cable may be powered from the VCONN supply or directly from VBUS and may draw up to 1.0W of total power.

> 管理型有源电缆是一种带有电子标记的电缆，还具有供电的 USB 数据修复电路。管理型有源电缆可由 VCONN 电源供电，或直接由 VBUS 供电，总功率最高可达 1.0W。

Use-case Example: An active cable that uses repeaters/re-conditioners to extend the maximum cable length.

> 用例示例：使用中继器/再调节器来延长最大电缆长度的有源电缆。

A managed active cable will behave identically to a standard active cable if inserted into a receptacle that does not support USB Power Delivery 2.0. It will still be able to power itself from VCONN or VBUS.

> 如果将管理型有源电缆插入不支持 USB Power Delivery 2.0 的插座，则其行为将与标准有源电缆相同。它仍然能够通过VCONN或VBUS为自己供电。

## 2.7 USB Type-C to Legacy USB Cables

The USB Type-C™ specification also defines the allowable USB Type-C to Legacy USB cable assemblies. The following full cable assemblies are supported:

> USB Type-C 规范还定义了允许的 USB Type-C™ 到传统 USB 电缆组件。支持以下完整电缆组件：

- USB Type-C to Type-A (USB2.0)
- USB Type-C to Type-A (USB3.0/3.1)
- USB Type-C to Type-B (USB2.0)
- USB Type-C to Type-B (USB3.0/3.1)
- USB Type-C to Mini-B (USB2.0)
- USB Type-C to Micro-B (USB2.0)
- USB Type-C to Micro-B (USB3.0/3.1)

Only two USB Type-C to Legacy adapters are defined:

> 仅定义了两个 USB Type-C 至传统适配器：

- USB Type-C to Type-A receptacle adapter
- USB Type-C to Micro-B (USB2.0)


# 3 CC PINS

The CC1 and CC2 pins are critical for basic USB Type-C operation. Resistors are attached to the CC pins in various configurations depending on whether the application is a downstream facing port (DFP), upstream facing port (UFP), or an electronically marked/active cable:

- Rp pull-up resistors on downstream facing ports (Section 3.1)
- Rd pull-down resistors on upstream facing ports (Section 3.2)
- Ra pull-down resistor on electronically marked/active cables (Section 3.3)
    

> CC1 和 CC2 引脚对于基本的 USB Type-C 操作至关重要。电阻器以各种配置连接到 CC 引脚，具体取决于应用是面向下游的端口 （DFP）、面向上游的端口 （UFP） 还是电子标记/有源电缆：
> 
> - 面向下游端口的 Rp 上拉电阻器（第 3.1 节）
> - 上游端口上的 Rd 下拉电阻器（第 3.2 节）
> - 电子标记/有源电缆上的 Ra 下拉电阻器（第 3.3 节）

The CC1 and CC2 pins must be constantly monitored by the port to perform the following functions:

- Cable attach and removal detection (Section 3.4)
- Cable orientation detection (Section 3.5)
- Basic USB Type-C current capability advertisement (Section 3.6)

> 端口必须持续监控 CC1 和 CC2 引脚才能执行以下功能：
> 
> - 电缆连接和拆卸检测（第 3.4 节）
> - 电缆方向检测（第 3.5 节）
> - 基本 USB Type-C 电流能力广告（第 3.6 节）

## 3.1 DFP Rp Pull-Up Resistors

The Rp pull-up resistors on a downstream facing port must be connected to both CC1 and CC2 pins, and may be pulled up to either 3.3V or 5.0V (a current source may also be used). The value of the resistor selected advertises the current supplying capability of the port to the device. The acceptable (per the USB Type-C™ specification) values for the Rp pull-up resistors and current sources are shown in the table below.

> 下游端口上的 Rp 上拉电阻必须连接到 CC1 和 CC2 引脚，并且可以上拉至 3.3V 或 5.0V（也可以使用电流源）。所选电阻的值向器件公布端口的电流供应能力。下表显示了 Rp 上拉电阻器和电流源的可接受值（根据 USB Type-C™ 规范）。

![[Pasted image 20240602151541.png]]

## 3.2 UFP Rd Pull-Down Resistors.

An upstream facing port must connect a valid Rp pull-down resistor to GND (or optionally, a voltage clamp) to both CC1 and CC2 pins. A 5.1kΩ ± 10% is the only acceptable resistor if USB Type-C charging of 1.5A@5V or 3.0A@5V is to be used. The details are shown in the table below.

> 面向上游的端口必须将有效的 Rp 下拉电阻连接到 GND（或可选的电压钳位）和 CC1 和 CC2 引脚。如果要使用1.5A@5V或3.0A@5V的USB Type-C充电，5.1kΩ±10%是唯一可接受的电阻。详细信息如下表所示。

![[Pasted image 20240602151547.png]]

## 3.3 Active Cable Ra Pull-Down Resistors

An active cable must connect an Ra resistor from the VCONN pin to GND. The Ra resistor may range from 800Ω to 1.2kΩ.

> 有源电缆必须将 Ra 电阻从 VCONN 引脚连接到 GND。Ra电阻范围为800Ω至1.2kΩ。

## 3.4 Cable Attach and Removal Detection

A cable attach is detected when either of the CC1 or CC2 pins detects a valid Rp/Rd connection. For a standard USB connection, only one of the CC1/CC2 pins may detect a valid Rp/Rd connection, not both.

> 当 CC1 或 CC2 引脚中的任何一个检测到有效的 Rp/Rd 连接时，将检测到电缆连接。对于标准 USB 连接，只有一个 CC1/CC2 引脚可以检测到有效的 Rp/Rd 连接，而不能同时检测两个引脚。

5V to VBUS may only be applied when a valid cable attachment is detected. This prevents two downstream facing ports from back-driving current into each other.

> 5V 至 VBUS 仅在检测到有效的电缆附件时才适用。这样可以防止两个面向下游的端口相互反向驱动电流。

![[Pasted image 20240602151556.png]]

## 3.5 Cable Orientation Detection（电缆方向检测）

The cable orientation is detected in the following way:

- If the CC1 pin detects a valid Rp/Rd connection, then the cable is in the “Unflipped” orientation at that receptacle.
- If the CC2 pin detects a valid Rp/Rd connection, then the cable is in the “Flipped” orientation at that receptacle.

> 通过以下方式检测电缆方向：
> 
> - 如果 CC1 引脚检测到有效的 Rp/Rd 连接，则电缆在该插座处处于“未翻转”方向。
> - 如果 CC2 引脚检测到有效的 Rp/Rd 连接，则电缆在该插座处处于“翻转”方向。

![[Pasted image 20240602151611.png]]

## 3.6 USB Type-C Current Advertisement（USB Type-C 电流广告）

Both the upstream facing port and the downstream facing port must monitor the voltage on the CC1 and CC2 pins to determine if a valid Rp/Rd or Rp/Ra connection has been made. The USB Type-C™ specification defines the following voltage ranges:

> 上行端口和下行端口都必须监控 CC1 和 CC2 引脚上的电压，以确定是否已建立有效的 Rp/Rd 或 Rp/Ra 连接。USB Type-C™ 规范定义了以下电压范围：

![[Pasted image 20240602151621.png]]

Once a valid connection is established, the upstream facing port (device) may is responsible for drawing the appropriate amount of maximum current.

> 一旦建立了有效的连接，面向上游的端口（设备）可能负责消耗适当的最大电流。

# 4 VCONN SUPPLY（VCONN供应）

VCONN is a 5V(4.75V - 5.5V allowable range) 1.0W power supply used to power circuits within the plug that are needed to implement electronically marked cables and VCONN-powered accessories. The DFP is responsible for supplying VCONN by default. If two Dual-Role ports with USB Power Delivery support are connected to each other, the VCONN supplier can be swapped via USB PD negotiation.

> VCONN 是一款 5V（4.75V - 5.5V 允许范围）1.0W 电源，用于为插头内的电路供电，这些电路需要实现电子标记电缆和 VCONN 供电附件。默认情况下，DFP 负责提供 VCONN。如果两个支持 USB Power Delivery 的双角色端口相互连接，则可以通过 USB PD 协商交换 VCONN 供应商。

VCONN is required for PD-enabled port and USB3 support. The VCONN power supply can be supplied in one of two ways:

> 支持 PD 的端口和 USB3 支持需要 VCONN。VCONN 电源可通过以下两种方式之一供电：

a) If a valid Rp/Rd connection is detected on one of the CC pins, the VCONN supply can be blindly routed to the opposite CC pin
b) After a valid Rp/Rd connection is detected on one of the CC pins, the opposite CC pin can be monitored for a valid Rp/Ra connection before routing the VCONN supply to the pin.

> a） 如果在其中一个 CC 引脚上检测到有效的 Rp/Rd 连接，则 VCONN 电源可以盲路由至对面的 CC 引脚
> b） 在其中一个 CC 引脚上检测到有效的 Rp/Rd 连接后，在将 VCONN 电源路由到该引脚之前，可以监控对面的 CC 引脚是否有有效的 Rp/Ra 连接。

Because of the reversible nature of the USB Type-C cable, both CC1 and CC2 pins must be able to assume the role of CC and VCONN upon cable insertion. A typical solution is presented in fig xx below.

> 由于 USB Type-C 电缆的可逆性，CC1 和 CC2 引脚在插入电缆时必须能够承担 CC 和 VCONN 的角色。典型的解决方案如下图 xx 所示。

![[Pasted image 20240602151632.png]]

Note: While all USB Type-C ports are required to source VCONN to active cables, active cables are permitted to source power from either VCONN or VBUS.

> 注意：虽然所有USB Type-C端口都需要将VCONN供电到有源电缆，但允许有源电缆从VCONN或VBUS供电。

# 5 USB POWER DELIVERY 2.0

USB Power Delivery 2.0 refers to a single wire protocol (on CC wire) created by the USB-IF. The name “USB Power Delivery” can be somewhat misleading as it allows for much more than just power negotiations; it unlocks the advanced capabilities of the USB Type-C cable. The PD messaging occurs completely independently of USB2.0 or USB3.0/USB3.1 data and is used for port-to-port negotiation of power roles, voltage level, maximum supplying current capability, data roles, and Alternate Modes. Port-to-powered cable communication is also handled by USB PD.

> USB Power Delivery 2.0 是指由 USB-IF 创建的单线协议（在 CC 线上）。“USB Power Delivery”这个名字可能有点误导，因为它允许的不仅仅是电源协商;它解锁了 USB Type-C 电缆的高级功能。PD 消息传递完全独立于 USB2.0 或 USB3.0/USB3.1 数据，用于电源角色、电压电平、最大供电电流能力、数据角色和备用模式的端口到端口协商。端口到供电电缆的通信也由 USB PD 处理。

## 5.1 Protocol Details（协议细节）

- All communication occurs over CC wire.
- The DFP is the Bus Master and initiates all communication.
- All messages are 32-bit 4b/5b encoded Bi-phase mark coded (BMC).
- 300k Baud rate
- CRC32 error detection + message retries
- Terminology:
    - SOP: DFP to DFP messaging
    - SOP’: DFP to active cable plug messaging
    - SOP’’: DFP to active cable plug messaging

> - 所有通信都通过 CC 线进行。
> - DFP 是总线主站，负责启动所有通信。
> - 所有报文均采用 32 位 4b/5b 编码双相标记编码 （BMC）。
> - 300k 波特率
> - CRC32 错误检测 + 消息重试
> - 术语：
>     - SOP：DFP 到 DFP 消息传递
>     - SOP'：DFP 到有源电缆插头消息传递
>     - SOP''：DFP 到有源电缆插头消息传递

![[Pasted image 20240602151642.png]]

Note: SOP’ is assigned to one plug of the cable while SOP’’ is assigned to the other. The cable plugs cannot tell which side that they are connected to, just that one end may respond to SOP’ addressed messages and the other may respond SOP’’ addressed messages.

> 注意：SOP'分配给电缆的一个插头，而SOP''分配给另一个插头。电缆插头无法分辨它们连接到哪一端，只是一端可以响应 SOP' 寻址消息，另一端可以响应 SOP" 寻址消息。

## 5.2 Power Delivery Negotiation

USB Power Delivery allows power configuration of a USB connection to be dynamically modified. The default 5V voltage on VBUS can be reconfigured up to any level up to 20V. The maximum current supplying capability can also be raised to a maximum of 5A with a 100W compatible electronically marked USB PD Type-C cable.

> USB Power Delivery 允许动态修改 USB 连接的电源配置。VBUS上的默认5V电压可以重新配置为最高20V的任何电平。使用兼容 100W 的E-Marked USB PD Type-C 电缆，最大电流供应能力也可以提高到最大 5A。

The default roles (Provider or Consumer) can also be dynamically swapped at any time if both ports support dual power role functionality and the port accepts the swap request.

> 如果两个端口都支持dual power role功能并且端口接受交换请求，则默认角色（提供者或使用者）也可以随时动态交换。

## 5.3 Alternate Mode and Data Role Negotiation.

Alternate Modes allow third party protocols to be transmitted over the USB Type-C cable. They are negotiated on port to port basis with Power Delivery protocol. See Section 6.0, Alternate Modes for more information.

> 备用模式允许通过 USB Type-C 电缆传输第三方协议。它们通过供电协议在端口到端口的基础上进行协商。有关更多信息，请参见部分 6.0， 备用模式。

Data roles can also be swapped dynamically over USB PD protocol negotiation.

> 数据角色也可以通过 USB PD 协议协商动态交换。

## 5.4 Billboard Device（广告牌设备）

Because of the wide range of capabilities enabled with USB PD, it can become confusing for the end user. There may be times when a user connects two devices and expects a different result than what actually occurs. To provide some amount of feedback to the user, a USB2.0 “Billboard” class device connected to the Power Delivery system can provide messages to the user that can explain errors or compatibility issues.

> 由于 USB PD 支持的功能范围广泛，因此最终用户可能会感到困惑。有时，用户连接两个设备并期望得到与实际发生的结果不同的结果。为了向用户提供一定程度的反馈，连接到供电系统的 USB2.0“Billboard”类设备可以向用户提供可以解释错误或兼容性问题的消息。

# 6.0 ALTERNATE MODES（备用模式）

Alternate Modes and USB Power Delivery are the two key features that will allow the USB Type-C cable to become a true “universal” cable. Alternate Modes allow the USB Type-C cable to be reconfigured to support third party protocols.

> 备用模式和 USB 供电是使 USB Type-C 电缆成为真正的“通用”电缆的两个关键功能。备用模式允许重新配置 USB Type-C 电缆以支持第三方协议。

This feature is enabled only if both ports support the USB Power Delivery protocol and are both compatible with the specific Alternate Mode.

> 仅当两个端口都支持 USB 供电协议并且都与特定的备用模式兼容时，才会启用此功能。

There are no specific limits on Alternate Modes. As long as the cable can support the third party protocol signaling while maintaining a USB2.0 connection, then the Alternate Mode can be implemented. The USB Type-C™ specification does not define any Alternate Modes; Each third party must maintain its own USB Type-C Alternate Mode specification.

> 备用模式没有特定限制。只要电缆能够支持第三方协议信令，同时保持USB2.0连接，就可以实现交替模式。USB Type-C™ 规范未定义任何备用模式;每个第三方都必须维护自己的 USB Type-C 备用模式规范。

Alternate Mode negotiation is performed via USB Power Delivery protocol on a port-to-port basis.

> 备用模式协商通过 USB 供电协议在端口到端口的基础上执行。

## 6.1 Reconfigurable Pins（可重构引脚）

All Alternate Modes must minimally maintain a USB2.0 and USB Power Delivery connection. The following pins/wires may be reconfigured for the use with the Alternate Mode.

> 所有备用模式必须至少保持USB2.0和USB供电连接。以下引脚/电线可能会重新配置以与备用模式一起使用。

![[Pasted image 20240602151653.png]]

## 6.2 Example: DisplayPort

DisplayPort was one of the first 3rd part protocols to be specified as a USB Type-C™ Alternate Mode. The DisplayPort Alternate mode supports the following modes of operation:

> DisplayPort是首批被指定为USB Type-C™备用模式的第三部分协议之一。DisplayPort备用模式支持以下操作模式：

• (2) Display Port lanes + (1) USB3.1 lane
• (4) Display Port lanes

![[Pasted image 20240602151659.png]]