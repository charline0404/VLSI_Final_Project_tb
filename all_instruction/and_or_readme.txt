//set r1 to 32-bit 1
ADDI r1, r1, 4095
ADDI r2, r2, 20
SLL r1, r1, r2
ADDI r1, r1, 4095
ADDI r2, r0, 8
SLL r1, r1, r2
ADDI r1, r1, 255
//test logical operand
OR r2, r0, r1//should be all 1
AND r3, r0, r1//should be all 0
SW r0, r2, 0
SW r0, r3, 4