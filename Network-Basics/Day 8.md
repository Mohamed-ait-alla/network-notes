# What is PoE (Power Over Ethernet)
**PoE** allows network cables to carry both **data** and **electrical power**, eliminating the need for separate power cords. This is particularly beneficial for devices like IP cameras, wireless access points, and VoIP phones.

## How PoE Works

The technology uses **IEEE standards** to deliver power over Ethernet cables. This is achieved by injecting **low-voltage DC** power into the Ethernet cable alongside the **data signal**.  A PoE-enabled device, known as a **Powered Device (PD)**, receives both data and power from a **Power Sourcing Equipment (PSE)** such as a PoE switch or injector.
> **Note:** you can check for power in a switch using this cli command `show power inline`

## Standards and Power Levels
- **IEEE 802.3af (PoE):** Delivers up to 15.4 watts per port (Type 1).
- **IEEE 802.3at (PoE+):** Provides up to 25.5 watts per port (Type 2).
- **IEEE 802.3bt (PoE++):** Offers up to 60 watts (Type 3) and 100 watts (Type 4) per port.

## Active vs Passive PoE

- **Active PoE:** The **PSE negotiates** with the device **before sending power**. **Safe** and **widely** used in enterprise networks.
- **Passive PoE:** **Always sends** power over the cable **without negotiation**. Not standards-compliant. Can damage non-compatible devices if misused.
> **Important:** Always check if your device supports passive PoE before using it, mixing passive power with non-passive gear can **fry** your equipment.

## Benefits of PoE
- **Simplified Installations**
- **Flexibility**
- **Cost-Effective**
- **Safety**