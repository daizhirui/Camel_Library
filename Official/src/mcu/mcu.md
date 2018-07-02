# Micro Control Unit (MCU) Library for M2  {#mcu}

To use this library, please include `mcu.h`.

## Interface

```C
long MemoryRead32(addr)；

void MemoryWrite32(addr,val)；

void MemoryOr32(addr,val)；

void MemoryAnd32(addr,val)；

void MemoryBitAt(addr,val)；

void MemoryBitOn(addr,val)；

void MemoryBitOff(addr,val)；

void MemoryBitSwitch(addr,val)；

void JumpTo(address)；

void RT_MCU_SetSystemClock(mode);

void RT_Clr_Sram();
```

## Example

```C
long a = MemoryRead32(0x1000000);      // read the value @0x1000000
JumpTo(0x1000000);                     // jump the program to the address 0x1000000
RT_Clr_Sram();                         // clear the 2kx32 sram space
```