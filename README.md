# AmoebaVirtualMachine
This is a VBA program that emulates a simple Von Neumann architecture computer.
<br>Download the latest release [here](https://github.com/TheOrangeCow/AmoebaVirtualMachineV2/releases/tag/v1)

### How it works?
It takes 8 bit binary code (00001111) and runs them.
The first 4 bits are the Operation Code and the other 4 bits are a number for a address location or a number

### Operation Code Set
This is the operation codes also find a pdf version <a href ="/TheAmoebaV2OperationCodeSet.pdf">Here</a>

| Opcode | Instruction | Description |
|------|------|-------------|
| 0000 | LDA | Load the Accumulator with the contents of the addressed location. |
| 0001 | STA | Store the contents of the Accumulator in the addressed location. |
| 0010 | LDAN | Load the Accumulator with the actual value of the address. |
| 0011 | ADD | Add the contents of the addressed location to the value in the Accumulator. The result is stored in the Accumulator. |
| 0100 | SUB | Subtract the contents of the addressed location from the value in the Accumulator. The result is stored in the Accumulator. |
| 0101 | MLT | Multiply the contents of the addressed location by the value in the Accumulator. The result is stored in the Accumulator. |
| 0110 | DIV | Divide the value in the Accumulator by the contents of the addressed location. The result is stored in the Accumulator (no remainder). |
| 0111 | JF | Jump forward a number of instructions. The number is given by the contents of the addressed location. |
| 1000 | JB | Jump back a number of instructions. The number is given by the contents of the addressed location. |
| 1001 | JFE | If the contents of the Accumulator is zero, jump forward a number of instructions given by the contents of the addressed location. |
| 1010 | JBE | If the contents of the Accumulator is zero, jump back a number of instructions given by the contents of the addressed location. |
| 1011 | CLR | Clear the output. |
| 1100 | OUTN | Display the contents of the Accumulator in the output as a number. |
| 1101 | OUTC | Display the contents of the Accumulator in the output as a character. |
| 1110 | NOP | No operation. |
| 1111 | END | End program execution. |

### Example code
<code>00100101
00010000
00100100
00010001
00000000
00110001
00010010
11110000
</code>
This code does 4 + 5 (= 9) and stores the output.

<code>
00101111
00010000
00101100
00010001
00110000
00110000
00110000
00110001
11000000
11110000
</code>
This code does 27 + 42 (= 69) and prints the output.

### Pictures  
<img width="397" height="325" alt="image" src="https://github.com/user-attachments/assets/0a3bfd81-6de6-4a02-9072-b7ecc6be3e8a" />
<img width="393" height="420" alt="image" src="https://github.com/user-attachments/assets/d20de13d-30fc-44ee-ac8b-b2e713762399" />
<img width="674" height="621" alt="image" src="https://github.com/user-attachments/assets/fabaecfb-6070-44a5-b8ed-84de7ca44759" />




