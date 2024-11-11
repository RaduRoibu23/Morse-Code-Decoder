# Morse Code Decoder Using a Turing Machine

The approach taken in this solution focuses on step-by-step decoding of Morse code using individual components of the Morse alphabet. The goal is to decode each "dot" and "dash" symbol, process spacing, and construct the final message efficiently on the Turing Machine tape.

## Strategy

1. **Individual Symbol Decoding**: 
   - The Morse code consists of individual components represented as "P" for dots (.) and "B" for dashes (-).
   - We start by decoding each symbol individually. For example, "P" represents a dot, while "PP" and "PPP" represent two and three dots in a row, respectively. Similarly, "B" and "BB" represent dashes of different lengths.

2. **Handling Spaces Between Letters and Words**:
   - Spaces in Morse code, such as short and long pauses between letters or words, are represented using sequences of "B" (bars).
   - These are processed and translated accordingly, ensuring that each group of "P" and "B" characters aligns with Morse code's dots and dashes.

3. **Constructing the Final Word**:
   - After decoding all Morse sequences on the tape, we arrange them to form the word. 
   - For readability, any unused sections on the tape are marked with the character `|` to clearly separate decoded symbols from the final message.

4. **Finalizing the Output on Tape**:
   - The decoded word is written to the tape at the end of the Turing Machine's operation, rather than the beginning, to keep the number of states low and simplify the process.
   - Using the `@` symbol as a marker, the Turing Machine traverses from left to right, writing the final message sequentially.
   - Once the message is complete, any remaining characters after the `@` marker are erased to leave a clean result on the tape.

## Reversing Key Words

We begin with the last character of the decoded word and search backward for specific key words. By examining the words in reverse order, we can ensure accurate identification and efficient state transitions.

---

This method provides a structured, efficient way to decode and construct messages in Morse code using a Turing Machine while minimizing the number of states required.
