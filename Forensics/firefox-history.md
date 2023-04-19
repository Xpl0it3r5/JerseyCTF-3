![](../Images/Pasted%20image%2020230419180421.png)

We got mozilla history in a `sqlite` file format.

I'm gonna use [sqlite-viewer](https://inloop.github.io/sqlite-viewer/) to view this file.

![](../Images/Pasted%20image%2020230419182632.png)

Select `moz_places` to view history

![](../Images/Pasted%20image%2020230419182749.png)

Here we found visited site and time, but time is in `UNIX Epoch` format.

Use [Unix-TimeStamp](https://www.unixtimestamp.com/) to decode `1674907264007000`. 

```ruby
FLAG : jctf{2023-01-28-12-01-04}
```
