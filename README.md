## GUIDE TO COMPILING AND EXECUTING CODE  

To run and compile assembly programs, ensure you have a suitable environment set up (e.g., NASM for x86 architecture). Follow these instructions for each task:  

1. **Compile the Assembly Code**  
   - For 64-bit systems:  
     ```bash  
     nasm -f elf64 <filename>.asm -o <filename>.o  
     ```  
   - For 32-bit systems:  
     ```bash  
     nasm -f elf32 <filename>.asm -o <filename>.o  
     ```  

2. **Link the Compiled Object File**  
   ```bash  
   ld <filename>.o -o <filename>  
   ```  

3. **Execute the Program**  
   ```bash  
   ./<filename>  
   ```  

> Replace `<filename>` with the actual name of the task file (e.g., `task1`, `task2`, etc.).  

---

### Task 1: Conditional Logic and Program Flow  
#### Summary  
This program determines whether a number entered by the user is "POSITIVE," "NEGATIVE," or "ZERO." It highlights the use of both conditional and unconditional jumps to control program execution.  

#### Key Challenges  
- **Using Jump Instructions:** Selecting between unconditional (`jmp`) and conditional jumps (`je`, `jl`, etc.) was crucial for accurate flow control.  
- **Branching Decisions:** The program required careful planning to handle the three scenarios without compromising stability.  

#### Takeaways  
- Conditional jumps effectively simplify decision-making by leveraging comparisons for branching.  
- Structuring the program into distinct sections improves readability and debugging efficiency.  

---

### Task 2: Reversing Arrays with Loops  
#### Summary  
This program accepts an array of integers, reverses its order in memory, and displays the reversed result. The reversal process is performed using a loop and avoids allocating extra memory.  

#### Key Challenges  
- **In-Place Reversal:** Reorganizing elements within the same memory space required precise memory addressing.  
- **Boundary Checks:** It was essential to iterate only halfway through the array to avoid errors like segmentation faults.  
- **Index Handling:** Managing pointers for the array's start and end required close attention to avoid overlapping.  

#### Takeaways  
- Register-based pointer arithmetic improves the program’s performance by reducing memory access.  
- Halving the number of iterations ensures the reversal process is efficient and avoids unnecessary computations.  

---

### Task 3: Factorial Calculation with Modular Subroutines  
#### Summary  
This task involves computing the factorial of a user-supplied integer using a dedicated subroutine. The subroutine uses stack operations to preserve registers and applies a loop to perform repeated multiplications.  

#### Key Challenges  
- **Register Preservation:** Using the stack to save and restore register values was crucial to maintaining program stability.  
- **Input Conversion:** Handling and validating ASCII input for conversion to an integer was necessary to prevent errors.  
- **Handling Large Values:** Factorial calculations produce large results, so input values near the upper limit required testing to avoid overflow.  

#### Takeaways  
- Subroutines improve code modularity and reusability by isolating functionality.  
- Proper stack management prevents interference with registers used in other parts of the program.  

---

### Task 4: Simulating Sensor-Control Systems  
#### Summary  
This program mimics a water level monitoring system. Depending on the simulated sensor’s input value, the program performs the following actions:  
1. Activates a "motor" when water is below the desired level.  
2. Stops the motor when the water level is optimal.  
3. Sounds an "alarm" when the water level exceeds the safe threshold.  

#### Key Challenges  
- **Port Simulation:** Representing input/output ports using memory locations required an innovative approach.  
- **Logic Design:** Implementing efficient branching mechanisms to handle low, moderate, and high water levels without ambiguity.  
- **Memory Mapping:** Correctly manipulating specific memory addresses to simulate sensor and motor interactions.  

#### Takeaways  
- Simulating hardware behavior through code provides a practical understanding of port-based systems without relying on actual hardware.  
- Using clear logic and modular programming makes it easier to debug and expand the system’s functionality.  
