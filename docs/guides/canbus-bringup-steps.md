# Bringing up CAN interface on linux machine

### Native Interfaces

In most cases you won't need to load the kernel driver for your real hardware. So let us concentrate on ip invocation:

the following lines set our canbus card to the correct bitrate 500000 and sets it in up mode.

```bash
 $ sudo ip link set can0 type can bitrate 125000
 $ sudo ip link set up can0
```

for more instrucctions go to:
https://elinux.org/Bringing_CAN_interface_up