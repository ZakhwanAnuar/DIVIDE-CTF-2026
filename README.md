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
![.](Forensics/Cant-Let-Go/question.png)

We are given an `.eml` file. The goal is to find the hidden flag inside the attachments sent via email. 

#### Step 1: Open the Email
Open the `.eml` file using Outlook. The email contains an attachment named `memories.pdf`.

![.](Forensics/Cant-Let-Go/email.png)

---

#### Step 2: Verify the Attachment
Attempting to open `memories.pdf` directly fails. Upon inspection, it turns out that the file is not a true PDF but actually a 7z archive.  

![.](Forensics/Cant-Let-Go/file.png)

Rename the file extension from `.pdf` to `.7z`:


---

#### Step 3: Extract the Archive
Extract `memories.7z`. After extraction, we get a folder named `flag` containing:

1. `letter.txt`
2. `loveYou.txt`
3. `ourPic`
4. `pantai.png`

![.](Forensics/Cant-Let-Go/list.png)

---

#### Step 4: Identify Correct File Extensions
Some files have incorrect extensions. After fixing them:

1. `ourPic.png`
2. `loveYou.7z`
3. `letter.png`
4. `pantai.png`

---

#### Step 5: Examine Files

##### ourPic.png
Opening `ourPic.png` reveals the first part of the flag:

![.](Forensics/Cant-Let-Go/ourPic.png)

*part1: divide{HoP3_wE_c4N_Be_bACk*

---

#### letter.png
`letter.png` contains a password: *theMoonisBeuty*


This password will be used for `loveYou.7z`.

![.](Forensics/Cant-Let-Go/letter.png)

---

#### pantai.png
No flag here, just an image for context.

![.](Forensics/Cant-Let-Go/pantai.png)

---

#### Step 6: Extract loveYou.7z
Use the password `theMoonisBeuty` to extract `loveYou.7z`. Inside, there is a PDF file.

![.](Forensics/Cant-Let-Go/flagpdf.png)

Opening the PDF appears blank, but selecting all text (CTRL + A) reveals the second part of the flag at the bottom:

*part2: _AS_B3Fore_i_miss_you_Say4ng}*

#### 🚩 Flag: divide{HoP3_wE_c4N_Be_bACk_AS_B3Fore_i_miss_you_Say4ng}

### Kelajuan aKa Speed
### Open Your Eyes
### Something Left Behind
### Alien Is Our Friend
### AlphaZer0
### Unusual Incident
### Echoes in the Disguise
### Malware or not?
