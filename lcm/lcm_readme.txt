//set number
ADDI r1, r1, 7
ADDI r2, r2, 4
//prepare for constantly adding
ADD r3, r0, r1
ADD r4, r0, r2
//check the relation of r1&r2
SLT r10, r1, r2
BEQ r10, r0, 28
//r1<r2
BEQ r3, r4, 48//loop start-1
ADD r3, r3, r1//constantly add r3
SLT r10, r4, r3
BEQ r10, r0, 8
//r4<r3
ADD r4, r4, r2//add r4
JAL r15, 2097132//back to loop start-1
//r1>r2
BEQ r3, r4, 24//loop start-2
ADD r4, r4, r2//constantly add r4
SLT r10, r3, r4
BEQ r10, r0, 8
//r3<r4
ADD r3, r3, r1//add r3
JAL r15, 2097132//back to loop start-2
SW r0, r3, 0/output lcm