## Slide 6: Memory Access - The Translation Layer

**The problem**: The guest program thinks it's writing to address `0x08048000`, but that might not be available on the host.

**The solution**: Every memory access goes through a translator:

```c
// When the guest wants to read 4 bytes from address X
static inline int ldl(void *ptr) {
#ifdef WORDS_BIGENDIAN
    // If host is big-endian but guest is little-endian
    // Swap the bytes around
    return p[0] | (p[1] << 8) | (p[2] << 16) | (p[3] << 24);
#else
    // If architectures match, just read directly
    return *(uint32_t *)ptr;
#endif
}
```

**Plain language**: It's like reading a book that's written right-to-left when you're used to left-to-right. The words are the same, but you need to flip them around to understand them.

## Slide 7: The Main Execution Loop - Like a Very Fast Interpreter

**Location**: `main.c:106` in `cpu_loop()`

This is the heart of the emulator. Here's what happens in simple terms:

```c
void cpu_loop(CPUX86State *env) {
    for(;;) {  // Forever loop
        err = cpu_x86_exec(env);  // Execute one instruction
        
        switch(err) {
            case EXCP0D_GPF:  // "General Protection Fault"
                // This usually means "the program tried to make a system call"
                if (is_syscall()) {
                    handle_syscall(env);  // Translate and execute
                }
                break;
                
            case EXCP_INTERRUPT:
                // "Hey, something external happened (like a signal)"
                handle_signals(env);
                break;
                
            // Other cases for different types of interruptions
        }
    }
}
```

**Real-world analogy**: This is like being a very fast translator at the United Nations. Someone speaks in x86 language, you translate it to ARM language, and vice versa, all in real-time.
