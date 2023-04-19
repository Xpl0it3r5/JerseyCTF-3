![](../Images/Pasted%20image%2020230419185829.png)

Lets visit the page first

![](../Images/Pasted%20image%2020230419185905.png)

Nothing other then this 'cool' page.

Lets look for `/flag`

![](../Images/Pasted%20image%2020230419190002.png)

mhmm... thats something interesting, looks like an API call.
Lets look at the source of home page

![](../Images/Pasted%20image%2020230419190138.png)

We got authentication ~~so called~~ token, `GdERHpBh3x`.
Now we know what we have to do.

Here is the flag

![](../Images/Pasted%20image%2020230419190254.png)

```ruby
FLAG : jctf{*MAJ0R-K3Y-AL3RT*}
```