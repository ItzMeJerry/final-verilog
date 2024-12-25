# FPGA Final Project: Tetris

## Author: 112321019

A Tetris game made using Verilog

## Display
Game are shown on 8x8 display

## Features
Operation like left right rotate down

Have all the block types I,O,T,L,I,Z,S

During fall, player can control the block with left and right

Falling will stop if collision

If one row is filled then clear the row and add 1 to score

End the game when blocks is stacked to the top

Reset switch that resets the game

Show score when score is changed

Score display 7-seg display

Quick drop feature

A switch for auto reset when game end

## PINs used on FPGA

| input/output | PIN     | I/O              | comment                              |
|--------------|---------|------------------|--------------------------------------|
| CLK          | PIN_22  | --               | clock (25 MHZ)                       |
| left         | PIN_64  | 4 BITS SW        | Left button                          |
| down         | PIN_65  | 4 BITS SW        | Down button                          |
| rotating     | PIN_66  | 4 BITS SW        | Rotate button                        |
| right        | PIN_67  | 4 BITS SW        | Right button                         |
| loop         | PIN_124 | 8 DIPSW (ON=LOW) | auto start game without button       |
| accumulate   | PIN_128 | 8 DIPSW          | won't reset score when end           |
| skip         | PIN_129 | 8 DIPSW (ON=LOW) | spent 1 score to smash falling block |
| SW           | PIN_132 | 8 DIPSW (ON=HI)  | pause and display score              |
| CLR          | PIN_133 | 8 DIPSW (ON=HI)  | clear 8x8 LED                        |
| COMM[0]      | PIN_68  | S0               |                                      |
| COMM[1]      | PIN_69  | S1               |                                      |
| COMM[2]      | PIN_70  | S2               |                                      |
| COMM[3]      | PIN_71  | EN               | NO/OFF the LED line                  |
| DATA_B[0]    | PIN_111 | CB1              |                                      |
| DATA_B[1]    | PIN_112 | CB2              |                                      |
| DATA_B[2]    | PIN_113 | CB3              |                                      |
| DATA_B[3]    | PIN_114 | CB4              |                                      |
| DATA_B[4]    | PIN_115 | CB5              |                                      |
| DATA_B[5]    | PIN_119 | CB6              |                                      |
| DATA_B[6]    | PIN_120 | CB7              |                                      |
| DATA_B[7]    | PIN_121 | CB8              |                                      |
| DATA_G[0]    | PIN_135 | CG1              |                                      |
| DATA_G[1]    | PIN_136 | CG2              |                                      |
| DATA_G[2]    | PIN_137 | CG3              |                                      |
| DATA_G[3]    | PIN_138 | CG4              |                                      |
| DATA_G[4]    | PIN_141 | CG5              |                                      |
| DATA_G[5]    | PIN_142 | CG6              |                                      |
| DATA_G[6]    | PIN_143 | CG7              |                                      |
| DATA_G[7]    | PIN_144 | CG8              |                                      |
| DATA_R[0]    | PIN_72  | CR1              |                                      |
| DATA_R[1]    | PIN_73  | CR2              |                                      |
| DATA_R[2]    | PIN_74  | CR3              |                                      |
| DATA_R[3]    | PIN_75  | CR4              |                                      |
| DATA_R[4]    | PIN_76  | CR5              |                                      |
| DATA_R[5]    | PIN_77  | CR6              |                                      |
| DATA_R[6]    | PIN_79  | CR7              |                                      |
| DATA_R[7]    | PIN_80  | CR8              |                                      |
| disp[0]      | PIN_59  |                  |                                      |
| disp[1]      | PIN_58  |                  |                                      |
| disp[2]      | PIN_55  |                  |                                      |
| disp[3]      | PIN_54  |                  |                                      |
| disp[4]      | PIN_53  |                  |                                      |
| disp[5]      | PIN_52  |                  |                                      |
| disp[6]      | PIN_51  |                  |                                      |
| sel[0]       | PIN_38  |                  |                                      |
| sel[1]       | PIN_39  |                  |                                      |
| sel[2]       | PIN_42  |                  |                                      |
| sel[3]       | PIN_43  |                  |                                      |

## Compilation Info

|                           |                                            |
|---------------------------|--------------------------------------------|
| Quartus II 64-Bit Version | 13.1.0 Build 162 10/23/2013 SJ Web Edition |
| Revision Name             | tetris                                     |
| Top-level Entity Name     | tetris                                     |
| Family                    | Cyclone III                                |
| Device                    | EP3C10E144C8                               |