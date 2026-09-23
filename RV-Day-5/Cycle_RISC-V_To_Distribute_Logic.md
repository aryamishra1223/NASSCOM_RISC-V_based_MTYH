he CPU datapath is now distributed across:

| Stage | Function |
| --- | --- |
| `@0` | PC generation |
| `@1` | Fetch + Decode |
| `@2` | Register File Read |
| `@3` | Execute + Register Write |

---

# Important Note

Most of the implementation for this lecture was already completed in the previous lecture while debugging and stabilizing the 3-cycle CPU pipeline.

This lecture mainly formalizes:
- stage partitioning
- logic redistribution
- RF macro timing alignment

rather than introducing entirely new functionality.

<img width="913" height="742" alt="Image" src="https://github.com/user-attachments/assets/dbb31288-f3fa-46ab-adc7-e88b2367e337" />

<img width="1837" height="965" alt="Image" src="https://github.com/user-attachments/assets/c90b275a-03a4-4529-bb3e-056958c0f256" />
<img width="1838" height="890" alt="Image" src="https://github.com/user-attachments/assets/94fbc2f9-653d-40fd-9a12-7055199b0964" />
<img width="1844" height="955" alt="Image" src="https://github.com/user-attachments/assets/1290a210-5d45-4ab4-8757-7f73414b5edf" />
<img width="1844" height="955" alt="Image" src="https://github.com/user-attachments/assets/97cf924c-4e93-44ad-a177-9474aa2983a2" />
<img width="1844" height="955" alt="Image" src="https://github.com/user-attachments/assets/3b905129-3b29-4194-9529-1c11d8b0a374" />
<img width="827" height="788" alt="Image" src="https://github.com/user-attachments/assets/d27155c6-c5d7-487d-b9ee-cc70e31a135e" />
