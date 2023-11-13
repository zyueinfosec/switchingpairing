# SWITCHINGPairing

SwitchPairing requires users to connect pre-pairing devices to the same power source and randomly press and release a switch to generate a shared secret. This protocol eliminates the need for additional peripherals and offers inherent defense against eavesdropping and replay attacks. We have implemented a prototype using two CC2640R2F development boards and conducted experiments to benchmark its security and usability. The results demonstrate that our protocol meets the security and efficiency requirements of various IoT applications.

### Overview

SwitchPairing addresses the security and cost challenges by establishing an auxiliary channel without dedicated input/output peripherals. It leverages the power source and built-in clocks, which are common features in IoT devices. The protocol's main steps are as follows:

- Users connect pre-pairing devices to the same power source (e.g., a plug).
- Pre-pairing devices enter pairing mode, identify each other through an open wireless channel like Bluetooth, and synchronize their built-in clocks.
- Users randomly switch the power source on and off several times, with the time intervals between switches recorded by the devices.
- These time intervals are used to generate fuzzy commitments, authenticating the pairing devices and securing the wireless communication channel.

![alt text](https://github.com/zyueinfosec/switchingpairing/blob/master/0018d5813fca6cf76be03421896e576.png)
