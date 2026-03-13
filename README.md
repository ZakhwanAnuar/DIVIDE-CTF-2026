# DIVIDE-CTF-2026

## 📑 Table of Contents

- [Forensics](#forensics)
  - [Can't Let Go](#Cant-Let-Go)
  - [Kelajuan aKa Speed](#kelajuanakaspeed)
  - [Open Your Eyes](#OpenYourEyes)
  - [Something Left Behind](#SomethingLeftBehind)
  - [Alien Is Our Friend](#AlienIsOurFriend)
  - [AlphaZer0](#AlphaZer0)
  - [Unusual Incident](#UnusualIncident)
  - [Echoes in the Disguise](#EchoesIntheDisguise)
  - [Malware or not?](#MalwareOrNot?)
## Forensics
### Can't Let Go
The challenge description states that the ZIP password can be found inside the **`PCAP file`**.

First and foremost, I opened the provided PCAP file using Wireshark.

While analyzing the packets, I looked for anything suspicious such as:

-unusual payloads
-readable strings
-encoded data

Eventually, I found a suspicious packet that contained a string which looked like Base64-encoded data.
![.](Forensics/FindAndOpen/wireshark.png)
ChatGPT identified that:

The string was Base64-encoded

After decoding once, it resulted in another Base64 string

This means the data was double-Base64 encoded
I copied the suspicious string from the packet payload and pasted it into my best friend — ChatGPT 😄 to help analyze it.
![.](Forensics/FindAndOpen/chatgpt.png)

**`rs is the secret: picoCTF{R3DING_LOKd_}`**

so i think that is the password.
![.](Forensics/FindAndOpen/flag.png)

and yess!!
#### 🚩 Flag: picoCTF{R34DING_LOKd_fil56_succ3ss_cbf2ebf6}
#
