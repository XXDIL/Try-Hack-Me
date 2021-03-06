# TASK 3 : RECONNAISSANCE

So we need to scrape the internet for any trace of this `username : SakuraSnowAngelAiko`. There is an amazing tool for just this its called [SHERLOCK](https://github.com/sherlock-project/sherlock), i would highly recommend this.

clone the repo and run it on the username, we willget the following results.

<img src="https://user-images.githubusercontent.com/66634743/115616829-b57b8d00-a301-11eb-82ef-08fa761e9635.png" width=700 height=100>

The first 2 links were pointless but the github link contained some interesing repos. After going through the low frequency repos (mainly because this is an easy CTF), these 3 repos caught my eye.

<img src="https://user-images.githubusercontent.com/66634743/115617665-b9f47580-a302-11eb-8a90-5364f61bdb58.png" width=700 height=300>



### 1) What is the full email address used by the attacker?

We are given a pgp public key in the PGP repo, this is huge because when u think about PGP the first thing that should come to mind in email encryption.

After a bit of searching, for how to get data from a pgp public key I found this -> [PGP-resource](https://www.oreilly.com/library/view/linux-security-cookbook/0596003919/ch07s26.html)

```console
foo@bas:~$ gpg --import key
```

![pgp](https://user-images.githubusercontent.com/66634743/115623151-de078500-a309-11eb-838f-2dbc0b27e198.png)

And there we go, we just found the EmailID.

### 2) What is the attacker's full real name?

As sherlock didn't give us anymore links, I decided to search the net on my own and sure enough i found a `linkedin` page.

![name](https://user-images.githubusercontent.com/66634743/115623145-db0c9480-a309-11eb-9ff3-d351a27fa20f.png)

Now we have the Name too 👍.
