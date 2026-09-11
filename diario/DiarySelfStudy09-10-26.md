# 🛡️ CyberStudy — 09/10/26

![Platform](https://img.shields.io/badge/Platform-TryHackMe-red)
![Topics](https://img.shields.io/badge/Topics-TLS%20%7C%20SSL%20%7C%20Wireshark-blue)

> Daily notes from my cybersecurity learning journey on **TryHackMe**.

Today was another day of studying with TryHackMe, and I wrapped up two rooms.

## 📑 Contents
- [🔐 Secure Protocols](#-secure-protocols)
- [🦈 Wireshark](#-wireshark)
- [💭 Final Thoughts](#-final-thoughts)

---

## 🔐 Secure Protocols

I finished the room about secure protocols today, which explained how **TLS** and **SSL** are used to encrypt data during transmission.

It started with a bit of history: back in the early 1990s, as the internet was taking off, there was a growing need to encrypt online communications to prevent data leaks. That's what led to **SSL** (Secure Sockets Layer), developed by **Netscape**, with its public version 2.0 released in 1995. Then in 1999, **TLS** (Transport Layer Security) came out as an upgrade to SSL 3.0, and it's still the protocol used to secure connections today. In 2018 TLS got a major update with version **1.3**, which is the version in use now.

After that intro, the room showed how old protocols get a secure version by adding encryption on top, like **HTTP** becoming **HTTPS**, or **SMTP** becoming **SMTPS**. It also walked through the process of getting a security certificate for a website, including **self-signed certificates**.

Next it went into how TLS works on top of HTTP, sitting at the transport layer of the **OSI model**, and showed a practical example of establishing a TLS session using a **GET** request while looking at the packets in **Wireshark**. It also covered the encryption key used by TLS — there's a single key needed to decrypt a packet or frame, and with the right key you can actually decrypt the file.

Then it covered the standard and secure versions of several protocols and which **ports** each one uses, since the secure versions run on different ports than the standard ones.

After that came **SSH** (Secure Shell), which uses a tunneling system to set up a secure session between a client and a server. The client is always the one requesting the session, and to open it you type a command with the correct info. SSH encrypts the data exchanged between client and server, which the room compared to **Telnet** (SSH's insecure predecessor) and to the kind of tunneling used by **VPNs**.

Then it moved to **FTP** (File Transfer Protocol) and its secure alternatives, **SFTP** and **FTPS**. SFTP uses Unix-like commands, which are different from the ones used by standard FTP.

The room wrapped up with **VPNs**, explaining how they're commonly used to connect different branches of a company to a central office. It got a bit more technical here, covering how a VPN connection works across different countries and how it may or may not use the client's public or private IP address.

---

## 🦈 Wireshark

The second room I finished today was about **Wireshark**. It introduced the tool, why it's used, and how the interface works. The main thing I took away is that Wireshark is purely a packet-sniffing tool — it can't alter or modify packets, it just captures and displays the traffic passing through a network the user selects.

Wireshark has a bunch of built-in tools for filtering and analyzing packets, letting you inspect the contents, see the type of request, and identify the protocol used at any given moment. It's clearly a very useful and important tool for security work. The room also covered **pcap** files, which are the files used to store and analyze captured network traffic, and explained the color coding Wireshark uses for different types of packets. There's also a traffic-sniffing feature and, something I didn't know existed, the option to merge multiple capture files to see packets from two captures happening at the same time — I thought that was pretty interesting. You can also export packets to save and review them later, and the room comes with its own capture file, `exercise.pcap`, used for the practice questions.

Digging deeper into packet details, I learned how to inspect frames, **MAC addresses**, the protocol and protocol version used, and basically everything about how a packet was sent and received, including the addresses of everyone involved. It also went a bit into IP addressing, **UDP** and **TCP**, common errors you might see during analysis, and how the protocol data and the protocols themselves are applied.

After that came a section on navigating between packets using filters — filtering by packet number, jumping straight to a specific packet, or searching by keyword to find packets containing it. You can bookmark packets, which I thought was a nice touch, and even add comments to specific ones for a deeper look later or to share with another analyst. You can also export just the packets you've selected into their own file, and apparently export the file objects carried inside those packets too, though that part is still a bit over my head. On top of that, you can change how timestamps are displayed to whatever format works best for the analyst.

The room ended with a section fully dedicated to packet filtering — capturing, analyzing, and viewing filters within the tool. It showed how to turn a packet into a filter, use conversation filters, apply colorization filters, and add a custom filter tied to a specific column so you can analyze that one detail across every matching packet. You can also follow a packet's full stream to see what's inside it, as long as it isn't encrypted, and there's a simpler display filter option as well.

---

## 💭 Final Thoughts

> Overall, I really liked both rooms. Wireshark is something I'd been wanting to dig into for a while, and it turned out to be more complex than I expected — I think I'll only really get the hang of it by using it regularly, so I'm planning to start analyzing everyday traffic with it and exploring more of its features.
>
> The secure protocols room was just as valuable, since basically every protocol in use today relies on TLS encryption. Encryption is honestly one of the most important parts of cybersecurity, since it's what keeps files and data safe, and considering how much of what we do today is essentially just files being sent around, that feels like a pretty fundamental thing to understand.

---

<p align="center"><i>That's all for today regarding my cybersecurity studies with TryHackMe, thanks for following along ☺️.</i></p>
