---
title: Supply Chain Risk
tags: is exam
---

*Notes: Copyrights belongs to the  individual/organisations from the source, all the content quoted in this post only aim to use for blogger’s personal subject case studies non-commercially*

*Source:* 
1. [Malicious updates for ASUS laptops | Kaspersky official blog](https://www.kaspersky.com/blog/shadow-hammer-teaser/26149/)
2. [ShadowHammer: A large-scale operation | Kaspersky official blog](https://www.kaspersky.com/blog/details-shadow-hammer/26597/)
## Supply Chain risk
Supply chain security refers to efforts to enhance cybersecurity. Supply chain security management involves the information technology systems, software, and networks, which are driven by threats such as super-terrorism, malware, data theft and he advanced persistent threat (APT)

At the end of January 2019, Kaspersky Lab researchers discovered what appeared to be a new attack on a large manufacturer in Asia. Our researchers named it “Operation ShadowHammer”.
Some of the executable files, which were downloaded from the official domain of a reputable and trusted large manufacturer, contained apparent malware features. Careful analysis confirmed that the binary had been tampered with by malicious attackers.

## ShadowHammer: Malicious updates for ASUS laptops
*Biggest supply-chain indidents ever.* 
### Threat - Trojanized utility 木马类实体
A threat actor modified the ASUS Live Update Utility, which delivers BIOS, UEFI, and software updates to ASUS laptops and desktops, added a back door to the utility, and then distributed it to users through official channels. A reddit post suggests evidences that potentially compromised updates were delivered to users as far back as June 2018.

It is important to note that any, even tiny, tampering with executables in such a case normally breaks the digital signature. However, in this case, the digital signature was intact: valid and verifiable. We quickly realised that we were dealing with a case of a **compromised digital signature.**

### Process
The trojanized utility was signed with a legitimate certificate (e.g. “ASUSTeK Computer Inc.”) and was hosted on the official ASUS server dedicated to updates, and that allowed it to stay undetected for a long time. The criminals even made sure the file size of the malicious utility stayed the same as that of the original one.

The attackers either had access to the source code of the victims’ projects or they injected malware at the time of project compilation, meaning they were in the networks of those companies. 


### Impact
More than 57000 users of Kaspersky Lab’t Products have installed the backdoor utility, but they estimate it was distributed to about 1 million people total. The cybercriminals behind it were not interested in all of them, however — they targeted only 600 specific MAC addresses, for which the hashes were hardcoded into different versions of the utility.
Also, that list of 600-plus MAC address did not limit the targets to 600 (plus); at least one of them belongs to a virtual Ethernet adapter. All users of that device share the same MAC address.

It was capable of gathering information about the system including usernames, computer specs, and operating system versions. It could also be used to download malicious payload from C&C servers, so unlike in the ASUS case, the list of potential victims was not limited to a list of MAC addresses.

### Potential Solutions
As of now, all Kaspersky Lab solutions detect and block the trojanized utilities, but we still suggest that you update the ASUS Live Update Utility if you use it. Our investigation is still ongoing.

### How to avoid becoming a link in a supply-chain attack
The common thread through all of the above mentioned cases is that attackers got valid certificates and compromised their victims’ development environments. 
Software vendors introduce another procedure into their software production process that additionally checks their software for potential malware injections even after the code is digitally signed

### Conclusions
While attacks on supply chain companies are not new, the current incident is a big landmark in the cyberattack landscape. Not only does it show that even reputable vendors may suffer from compromising of digital certificates, but it raises many concerns about the software development infrastructure of all other software companies.

ShadowPad, a powerful threat actor, previously concentrated on hitting one company at a time. Current research revealed at least four companies compromised in a similar manner, with three more suspected to have been breached by the same attacker. How many more companies are compromised out there is not known. What is known is that ShadowPad succeeded in backdoor developer tools and, one way or another, injected malicious code into digitally signed binaries, subverting trust in this powerful defence mechanism.

*Note: ShadowPad is one of the largest known supply-chain attacks. Had it not been detected and patched so quickly, it could potentially have targeted hundreds of organisations worldwide.*

#### Does it mean that we should stop trusting digital signatures?
**No.** But we definitely need to investigate all strange or anomalous behaviour, even by trusted and signed applications. Software vendors should introduce another line in their software building conveyor that additionally checks their software for potential malware injections even after the code is digitally signed.


