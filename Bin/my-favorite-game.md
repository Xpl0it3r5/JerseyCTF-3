![](../Images/Pasted%20image%2020230419151225.png)

- Using a python script got the flag
```python
from pwn import *
 
p = remote('0.cloud.chals.io', 22980)

up = lambda : p.sendlineafter(b"down?\n", b"up")
down = lambda : p.sendlineafter(b"down?\n", b"down")
left = lambda : p.sendlineafter(b"down?\n", b"left")
right = lambda : p.sendlineafter(b"down?\n", b"right")

up()
up()
down()
down()
left()
right()
left()
right()

p.interactive()
```
``` 
OUTPUT
python3 solve.py
[+] Opening connection to 0.cloud.chals.io on port 22980: Done
[*] Switching to interactive mode
jctf{K0nami_C0d3_w0rks_h3r3_t00}
Wait, why did that work?
```

```ruby
FLAG : jctf{K0nami_C0d3_w0rks_h3r3_t00}
```