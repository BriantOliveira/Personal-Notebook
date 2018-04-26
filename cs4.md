## Class 1: Bit Manipulation

Bitwise Operations

And **&**

Or **\|**

XOR **^ \(**Either one of the other**\)**

NOT** ~ \(**Flips the value**\)**

LEFT SHIFT **&lt;&lt;**

RIGHT SHIFT **&gt;&gt;**

**And** - Only true if both input bits are true

0 & 0 = 0

1 & 0 = 0

0 & 1 = 0

1 & 1 = 1

**XOr** - True if any input bit is true

0 \| 0 = 0

1 \| 0 = 1

0 \| 1 = 1

1 \| 1 = 0

**Left shift **-  Shift the binary digits by n, pad 0's on the right. Each shift is a multiply 2 \(unless there's overflow\)

```
00010110
<<
00000010
_________
01011000
```

**Right shift** - Shift the binary digits by n, pad 0's on the right. Each shift is a divide by 2 with round towards negative infinity.

**Set Bit**

```
int setBit(int x, unsigned char position) {
    int mask = 1 << position; 
    return x | mask;
}
```

**Clear Bit**

```
int clearBit(int x, unsigned char position) {
    int mask = 1 << position;
    return x & ~mask;
}
```

**Flip Bit**

```
int flipBit(int x, unsigned char position) {
    int mask = 1 << position;
    return x & ^mask;
}
```

Is Bit Set

```
bool isBitSet(int x, unsigned char position) {
    int shifted = x << position;
    return shifted x & 1;
}
```

Modify a Bit

```
int modifyBit(int x, unsigned char position, int state) {
    int mask = 1 << position;
    return (x & ~mask) | (-state & mask;
}
```



