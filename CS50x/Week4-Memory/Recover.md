# Problem Set 4: Recover

## Problem Overview
In this project, I wrote a program to recover "deleted" JPEGs from a forensic image of a memory card. Even though the file system may mark the space as free, the raw data remains. The goal was to scan the raw bytes of a memory card and reconstruct the image files.

## Key Concepts Learned
* **Pointers:** Using pointers to navigate through raw memory and handle data buffers.
* **File I/O:** Opening, reading, and writing to binary files using `fopen`, `fread`, and `fwrite`.
* **Hexadecimal Headers:** Identifying JPEG files by their unique "magic bytes" (`0xff 0xd8 0xff` followed by an `0xe...` byte).
* **Buffer Management:** Reading data in 512-byte blocks to mimic how memory cards store data.

## Algorithmic Thinking
The logic requires a continuous scan of the memory card file:
1. **Open** the forensic image file.
2. **Read** 512 bytes into a buffer.
3. **Check** the first 4 bytes for the JPEG signature.
4. **If a new JPEG is found:** - Close the previous file (if any).
    - Open a new file with a formatted name (e.g., `001.jpg`).
    - Start writing the buffer data.
5. **If already writing a JPEG:** Keep writing the blocks until a new header is found.
6. **Repeat** until the end of the card.
