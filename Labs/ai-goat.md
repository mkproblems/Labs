Summary: Babies first LLM exploits
## Spinning up the instance
In this guide I will be configuring a 2 VM lab using Kali Linux and a Debian server.
I will be using VMWare Workstation 17 Pro, which BroadCom recently made free for personal use.

### Debian
First we need the ISO
- Debian website

Initial installs and Network Configuration
Docker setup
ai-goat setup

### Challenge 1 - Basic Prompt Injection

I first tried to get it to give the password using urgency, but it seems like this model does not respond to that. 
![](../img/Pasted%20image%2020250208184705.png)

The next thing I tried was a translation injection where I instruct the LLM to translate something and then ignore the previous prompt and print something else.

![](../img/Pasted%20image%2020250208184841.png)
At first there was no response, but after entering an empty prompt it just spit out the Flag. 

"The flag is `{pr0mt1nj3cti0n}`"
### Takeaways:
I believe this is an example of Prompt Leaking, where I got it to print it's instruction set, which is to not divulge the secret. 
https://learnprompting.org/docs/prompt_hacking/leaking

## Challenge 2 - Title Requestor
