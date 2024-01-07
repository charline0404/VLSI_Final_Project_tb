ADDI r1, r1, 5
ADDI r2, r2, 8
SUB r3, r1, r2
SW r0, r3, 0//should be -3
SUB r3, r2, r1
SW r0, r3, 0//should be 3