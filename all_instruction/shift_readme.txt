ADDI r1, r1, 1//set r1 to 1
ADDI r2, r2, 7//set r2 to 7
SLL r1, r1, r2
SW r0, r1, 0//should be 256 in decimal
SRL r1, r1, r2
SW r0, r1, 0//should be 1 in decimal
