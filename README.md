# DIVIDE-CTF-2026

## 📑 Table of Contents

- [Forensics](#forensics)
  - [Can't Let Go](#cant-let-go)
  - [Kelajuan aKa Speed](#kelajuan-aka-speed)
  - [Open Your Eyes](#open-your-eyes)
  - [Something Left Behind](#something-left-behind)
  - [Alien Is Our Friend](#alien-is-our-friend)
  - [AlphaZer0](#alphazer0)
  - [Unusual Incident](#unusual-incident)
  - [Echoes in the Disguise](#echoes-in-the-disguise)
  - [Malware or not?](#malware-or-not)
## Forensics

### Can't Let Go
![.](Forensics/FindAndOpen/wireshark.png)

#### 🚩 Flag: picoCTF{R34DING_LOKd_fil56_succ3ss_cbf2ebf6}

### Kelajuan aKa Speed
### Open Your Eyes
### Something Left Behind
### Alien Is Our Friend
### AlphaZer0
### Unusual Incident
### Echoes in the Disguise
### Malware or not?
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
