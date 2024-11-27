ALP CAT 2

## HOW TO RUN AND COMPILE CODE  

- Ensure you have an assembly programming setup (e.g., NASM for x86).  
- Follow these steps for each task:  

1. **Assemble the code:**  
   - For 64-bit programs:  
     ```bash  
     nasm -f elf64 <filename>.asm -o <filename>.o  
     ```  
   - For 32-bit programs:  
     ```bash  
     nasm -f elf32 <filename>.asm -o <filename>.o  
     ```  

2. **Link the object file:**  
   ```bash  
   ld <filename>.o -o <filename>  
   ```  

3. **Run the executable:**  
   ```bash  
   ./<filename>  
   ```  

- Replace `<filename>` with the specific task file name (e.g., task1, task2, etc.).  

---

### Task 1: Control Flow and Conditional Logic  
#### Overview  
This program classifies a user-input number as "POSITIVE," "NEGATIVE," or "ZERO." It demonstrates effective control flow using conditional and unconditional jumps.  

#### Challenges  
- **Jump Instructions:** Understanding when to use unconditional jumps (`jmp`) versus conditional ones like `je` or `jl` was essential.  
- **Branching Logic:** Handling three distinct cases (positive, negative, zero) required careful program structure to maintain stability.  

#### Insights  
- Conditional jumps streamline logic by branching directly based on comparison results.  
- Dividing logic into modular blocks improves readability and debugging efficiency.  

---

### Task 2: Array Manipulation with Looping and Reversal  
#### Overview  
This program takes an integer array as input, reverses it in place, and outputs the reversed array. It uses a loop to swap elements without additional memory allocation.  

#### Challenges  
- **Memory Manipulation:** Swapping elements in place demanded precise handling of memory addresses.  
- **Bounds Checking:** Correctly iterating only halfway through the array was crucial to avoid segmentation faults.  
- **Indexing Complexity:** Managing pointers for both ends of the array required careful synchronization to avoid overlaps.  

#### Insights  
- Using registers for pointer arithmetic reduces memory operations and improves performance.  
- Iterating over half the array length ensures efficient and redundant-free swaps.  

---

### Task 3: Modular Program with Subroutines for Factorial Calculation  
#### Overview  
This program calculates the factorial of a user-input number using a subroutine. The subroutine employs the stack to preserve registers and a loop for multiplication.  

#### Challenges  
- **Register Management:** Properly saving and restoring registers using the stack ensured program stability.  
- **Input Conversion:** Converting ASCII input to an integer required robust validation to avoid errors.  
- **Overflow Risks:** Testing inputs near the integer storage limit was necessary due to the rapid growth of factorial values.  

#### Insights  
- Subroutines enhance code modularity and reusability.  
- Effective stack management ensures the integrity of registers across the program.  

---

### Task 4: Data Monitoring and Control Using Port-Based Simulation  
#### Overview  
This program simulates a water level monitoring system. Depending on the sensor value, it performs the following actions:  
1. Activates a "motor" when the water level is low.  
2. Deactivates the motor when the water level is moderate.  
3. Triggers an "alarm" if the water level is too high.  

#### Challenges  
- **Simulating Ports:** Mapping memory locations to mimic input/output ports required innovative solutions.  
- **Logic Implementation:** Efficient branching was essential to handle the three conditions (low, moderate, high) while ensuring clarity.  
- **Memory Addressing:** Managing memory locations to represent sensor and motor states required careful attention.  

#### Insights  
- Simulations offer a practical understanding of port-based systems without needing physical hardware.  
- Modular design and clear branching logic facilitate debugging and allow for functionality expansion.  
