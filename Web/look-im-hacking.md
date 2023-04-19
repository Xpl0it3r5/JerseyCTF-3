![](../Images/Pasted%20image%2020230419184203.png)

On visiting the site we find a login page, with pretty good security it seems ` : | `

![](../Images/Pasted%20image%2020230419184503.png)

Basically what this script is doing is that:
 - `createpass()` - it creates the random string as a password
 - `checkPass()` - it checks if username is `admin` and password is the string generated previously, then it calls `loadFlag()`
 - `loadFlag()` - it prints the `flag.txt` content

We can do 2 things here
1. Directly call the function manually
![](../Images/Pasted%20image%2020230419184922.png)

2. Or goto `https://www.jerseyctf.online/flag.txt`  and view the flag.

We called the function and got the flag content

![](../Images/Pasted%20image%2020230419185050.png)

```ruby
FLAG : jctf{$Hacker&?r3@L$}
```
