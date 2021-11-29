# VESC CAN BUS Command

## CAN characteristics

* Baud rate : 500kbit/s
* Signal update rate : 50Hz
* Data frame : Extended frame format

## CAN BUS CMD Reference

[VESC6 CAN Commands Telemetry](https://drive.google.com/file/d/1MUcwEVRscT-Bcs0xBAadZI1-tkqgKwdy/view?usp=sharing)

### Ex:Set Duty

ID : 0x00A (Extend frame format)
First"0" :

```c
CAN_PACKET_SET_DUTY = 0
```

Remaining 0A :
VESC ID (App Settings :arrow_right: General), Let's set Mid-Drive controller to 10 (0xA)

#### Data Field

![data](https://i.imgur.com/nIXnq5N.png)

## Mid-Drive VESC (ID : 10)

### Mid-Drive Motor Speed CMD

```c
CAN_PACKET_SET_RPM = 3
```

ID : 0x30A(Extend frame format)
Scale : 1

#### Data field(RPM)

![RPM](https://i.imgur.com/lOVbLgz.png)

### Brake Servo Position CMD(Requires custom firmware)

```=C
CAN_PACKET_SET_BRAKE_SERVO_POS = 46
```

ID : 0x2E0A(Extend frame format)
Scale : 0.01 (From 0-100)

#### Data field(Brake Servo)

![Servo](https://i.imgur.com/SwE56ga.png)

## Steering VESC (ID : 12)

### Steering Motor Speed CMD

```c
CAN_PACKET_SET_RPM = 3
```

ID : 0x30C(Extend frame format)
Scale : 1

#### Data field(Steering)

![Steering](https://i.imgur.com/lOVbLgz.png)
