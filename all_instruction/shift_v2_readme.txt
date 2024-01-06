ADDI r1, r1, 1//set r1 to 1
ADDI r2, r2, 31//set r2 to 31
SLL r1, r1, r2//r1 = 1<<31
SW r0, r1, 0//should be 2^31
SRL r1, r1, r2//r1 = 1>>31
SW r0, r1, 4//should be 1
ADDI r2, r2, 1//set r2 to 32
SLL r1, r1, r2//r1 = 1<<32
SW r0, r1, 8//should be 0
ADDI r1, r1, 1//set r1 to 0
ADDI r2, r0, 1//set r2 to 1
SRL r1, r1, r2//r1 = 1>>1
SW r0, r1, 12//should be 0
