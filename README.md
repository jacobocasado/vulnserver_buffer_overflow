# vulnserver_buffer_overflow
Buffer overflow for the Vulnserver server hosted on my own machine. 
Vulnserver: https://github.com/stephenbradshaw/vulnserver

It was a great learning lesson on how to do a basic buffer overflow.

Phase 1: Spiking -> We found the "FRUN" functions makes a buffer overflow.
Phase 2: Fuzzing -> On that function, we are going to see at what byte length of the payload does it crash.
  Once known, we will insert shellcode until the EIP code starts, and replace the EIP code to a "JMP ESP" function, followed by our code that will execute when we reach this part.
Phase 3: Finding bad characters -> We need to know what character does the program accept and what character doesn't like.
Phase 4: Exploit launch.

This is a very short summary of the process. 
My intention is to write the full proccess but I will need more time.
