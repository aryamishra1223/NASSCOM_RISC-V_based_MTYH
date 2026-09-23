# Address Generation

Load/store addresses are computed using:
```text
Address = rs1 + immediate
```
This is identical to the ADDI computation already implemented earlier. The address generation uses:

- source register 1 as base pointer
- immediate as offset

---

# Load Latency Problem

Unlike ALU instructions, memory does not immediately return data. The load data becomes available only after multiple cycles. This creates a new pipeline hazard:
```text
Load →
Instruction 1 →
Instruction 2
```
The instructions following load may attempt to use data before it has actually been written into the register file.

---

# Load Shadow

To solve this, the CPU introduces a load shadow. The two instructions immediately after the load are invalidated. This creates empty slots that allow:

- memory data to return
- register file write to complete
- bypass paths to receive updated data

This mechanism is conceptually similar to the earlier branch shadow.

---

<img width="827" height="788" alt="Image" src="https://github.com/user-attachments/assets/25f98ca7-658d-4d26-b8e7-48ade55d2246" />

<img width="827" height="893" alt="Image" src="https://github.com/user-attachments/assets/5942541c-3d42-4b20-b56d-41357cd15cc0" />
<img width="827" height="893" alt="Image" src="https://github.com/user-attachments/assets/124361d9-b87f-4574-a0af-548fea09a58f" />
<img width="1834" height="910" alt="Image" src="https://github.com/user-attachments/assets/cb259623-810a-4d36-a56d-8291f0012801" />
<img width="1849" height="891" alt="Image" src="https://github.com/user-attachments/assets/ca5e6609-da00-46df-9e49-8697b75ff6c3" />
<img width="963" height="890" alt="Image" src="https://github.com/user-attachments/assets/3ec5345e-36aa-4531-b5e8-16b80e7dc7cd" />
<img width="1847" height="890" alt="Image" src="https://github.com/user-attachments/assets/108e7347-0595-4f94-99dc-0d1c208b4d0c" />
<img width="1847" height="890" alt="Image" src="https://github.com/user-attachments/assets/80abeb5c-8e3e-456d-a988-173af194e38c" />
<img width="1847" height="890" alt="Image" src="https://github.com/user-attachments/assets/30140fce-ad98-4dcf-8e56-d151898305c9" />
<img width="1847" height="890" alt="Image" src="https://github.com/user-attachments/assets/11c1a82f-84a0-4510-a21a-6ff17e85806f" />
<img width="1847" height="890" alt="Image" src="https://github.com/user-attachments/assets/500d629d-fdd7-4375-9ea4-3f86f189a6db" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/e039eab4-267b-4b52-b8ca-ce615c2b8528" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/b9656954-e010-482e-ac91-b1123560dd00" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/d31e2edb-e9ee-49b4-84bd-827b3c136e35" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/90816685-3236-4ff3-91b7-83e9a268dd34" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/53f7346a-041e-4cb6-9924-34f1981948fd" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/f10a2680-5514-4ea1-82d5-1b2a2558f7ff" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/57f6e615-6451-4200-8b2e-aa998cb902cc" />
<img width="1847" height="923" alt="Image" src="https://github.com/user-attachments/assets/97825ef3-4540-4d2e-a47e-4d12fb1920f1" />
