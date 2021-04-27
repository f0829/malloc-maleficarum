# Malloc Maleficarum

| Technique                        | Description                                                                                                                               |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| fastbin double free              | Tricking malloc into returning an already-allocated heap pointer by abusing the fastbin freelist.                                         |
| fastbin double free into stack   | Tricking malloc into returning a nearly-arbitrary pointer by abusing the fastbin freelist.                                                |
| fastbin consolidated double free | Tricking malloc into returning an already-allocated heap pointer by putting a pointer on both fastbin freelist and unsorted bin freelist. |
| unsafe unlink                    | Exploiting free on a corrupted chunk to get an arbitrary write.                                                                           |
| house of spirit                  | Frees a forged fastbin chunk to get malloc to return a nearly-arbitrary pointer.                                                          |
| null-byte poisoning              | Exploiting a single null byte overflow.                                                                                                   |
| house of einherjar               | Exploiting a single null byte overflow to trick malloc into returning a controlled pointer.                                               |
| house of mind                    | Exploiting a single byte overwrite with arena handling to write a large value (heap pointer) to an arbitrary address.                     |
| large bin attack                 | Exploiting the overwrite of a freed chunk on large bin freelist to write a large value into arbitrary address.                            |
| mmap overlapping chunks          | Exploit an in use mmap chunk in order to make a new allocation overlap with a current mmap chunk.                                         |


Almost all the examples here were taken from the shellphish team's "how2heap" repository:
https://github.com/shellphish/how2heap
