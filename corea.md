**Random - Access Memory:**

Volatile - data in memory is cleared with power loss. 

RAM contains working space to run program and read/write data. Contains main stack and heap of program memory. 

Word\(unit\) locations addressed with sequential integers. 



**CPU Operation Loop :**



**Fetch** instruction form memory \(or cache\).

**Decode** instruction into opcode+ operands \( may require fetching data from memory\).

**Execute** instruction on data in registers.



**CPU instructions :**

Instructions are written in machine code Binary\). 

Single word\(typically 32 or 64 bits\) encodes: 

**Opcode** - Specifies operation to execute

**Operands** - 

**Instructions Type**:  

* Arithmetic\(add, subtract, multiply, devide\), 
* Logical \(and or, inverts, shift, rotate\), 
* Branch \(conditional, loop, function,\) 
* Memory \(load - read -, store - write\).

**Addressing modes**

immediate - operand is numerical value \(actual data\). 

Direct - operand specifies register containing data. 

Indirect - operand specifies memory address of data. 

Indexed - operands specify base memory address and offset of data. 



Memory address is even numbers because since the computer only execute in binary. So the compute knows that the next to are instructions. 

| Memory Address | Opcode | Operand |
| :--- | :--- | :--- |
| 0 | \(0\)   Load | \(1\)    \#2 |
| 2 | \(2\)    Add | \(3\)   \#3 |
| 4 | \(4\)   Store | \(5\)  @ 100 |
| 6 | Stop |  |

.

| 99 |  |
| :--- | :--- |
| 100 |  |
| 101 |  |



| Program Counter  |
| :--- |
| ~~0246~~ |



| Accumulator |
| :--- |
| ~~? 2 5~~ |





