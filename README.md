*This project has been created as part of the 42 curriculum by roandrie*

<p align="center">
  <img src="assets/logo.png" width="260" />
</p>
<h3 align="center">
  <em>Discover the basics of networking</em>
</h3>

---

<div align="center">
  <img src="https://img.shields.io/badge/SCORE-None-%235CB338?style=for-the-badge&logo=42&logoColor=white"/>
  <img src="https://img.shields.io/badge/COMPLETED-No-%23007ACC?style=for-the-badge&logo=calendar&logoColor=white"/>
</div>

## ⚠️ Disclaimer

- **Full Portfolio:** This repository focuses on this specific project. You can find my entire 42 curriculum 👉 [here](https://github.com/Overtekk/42).
- **Subject Rules:** I strictly follow the rules regarding 42 subjects; I cannot share the PDFs, but I explain the concepts in this README.
- **Archive State:** The code is preserved exactly as it was during evaluation (graded state). I do not update it, so you can see my progress and mistakes from that time.
- **Academic Integrity:** I encourage you to try the project yourself first. Use this repo only as a reference, not for copy-pasting. Be patient, you will succeed.

---

## 📂 Description

This project is an introduction to the basics of computer networking. We have a web server to do 10 exercices. Each of those exercices teach us one thing like how IP addresses works, how to connect a device throught a router, what is the role of a gateway.

---

## 💡 Instructions

To launch the exercice download the `net_practice.tgz` package **(only available for 42 student)**.\
One done, run the file `run.sh` using:
```bash
./run.sh
```
It will launch the web server using your default browser.

You can do two things.

- **Training**: Section to discover the world of computer networking and exercices to do. There are 10 exercices to subit.\
First thing first, enter your intranet login.\
Then, you will have to do the exercice (more of that later).\
You can click on `Check again` to check your current progression (errors, finished).\
`Get my config` give you the download to your configuration. This is needed for submission.\
If you have completed the level, click on the `Next level` button.

- **Evaluation**: This section is for the evaluation. Three randoms levels from 6 to 10 will be offered to be solved in 15 minutes.\
Then, it's all the same from above.

---

## 📥 Submission details


---

## 📝 Explanations of concepts

### IP: Network Layer

**Internet Protocol** or **Internet Protocol Adress**

</br>
<p align="center">
	<img src="assets/ip.png" height=100 alt="ip">
</p>
</br>

An IP adress is the **unique identifying number** assigned to every device connected to the internet or to a network. An IP adress definition is a numeric label assigned to devices that use the internet to communicate.
Its set a suite of rules for packetizing, addressing, transmitting, routing and receiving data over networks.

Its purpose is to handle the connection between devices that send and receive data all across the network.\
IP is unique to every device on the internet. It's an identifier. It allow computing devices to communicate with destinations like websites, streaming services letting the website know who is connecting.

An IP address has two parts. The first part identifies the host (such as the computer), and the other part identifies the network it belongs to. TCP/IP uses a **subnet mask** to separate them.

There are two important types of IP address:

- **Static IP address**: stay permanent and doesn't change. Mostly used for important equipement such as servers for example.
- **Dynamic IP address**: which changes occasionally. Used for consumer equipement such as computer, smartphone.

#### **IP addresses come in 2 versions:**

## IPv4 vs IPv6

</br>
<p align="center">
	<a href="https://www.avg.com/fr/signal/ipv4-vs-ipv6">
	<img src="assets/ipv4_vs_ipv6.png" height=200 alt="ipv4_vs_ipv6">
	</a>
</p>
</br>

**Internet Protocol version 4** defines an IP address as a 32-bit number and dot-decimal notation. Deployed in the 1981, it has over 4.3 billion addresses. Because of that, addresses must be reused and masked and must be configured manually./
However, because of the growth of the Internet and the depletion of available IPv4 addresses, a new version of IP as be created.

**Internet Protocol version 6** use 128 bits for the IP address and was standardized in 1998. It has over 340 undecillion addresses, so every device can have it's unique IP address, support auto-configuration and has alphanumeric hexadecimal notation.

**Only IPv4 addresses are used in NetPractice.**

## Public IP vs Private IP

- **Public IP** address can be accessed directly over the internet and is assigned to your network router by your internet service provider (ISP). It helps you connect to the internet from inside your network to outside your network.

- **Private IP** address that your network router assigns to your device. Each device within the same network is assigned a unique private IP address (sometines, also called a private network address). This is how devices on the same internal network talk to each other./
When a network is connected to the internet, it cannot use an IP address from the reserved private IP addresses. The following ranges are reserved for private IP addresses.

```
192.168.0.0 – 192.168.255.255 (65,536 IP addresses)
172.16.0.0 – 172.31.255.255   (1,048,576 IP addresses)
10.0.0.0 – 10.255.255.255     (16,777,216 IP addresses)
```


### TCP: Transport Layer

**Transmission Control Protocol** *(protocole de contrôle des transmissions).

</br>
<p align="center">
	<a href="https://github.com/lpaube/NetPractice/blob/main/img/tcp-ip-stack.png">
	<img src="assets/tcp_schema.png" height=300 alt="tcp_schema">
	</a>
</p>
</br>

It's a communication norm that allow application programs and devices to exchanges messages over a network. It's use to send packets across the internet.

It guarantees the integrity of the data being communicated over a network. Before it transmits data, TCP establishes a connection between a source and its destination, which remains active until communication begins. It then breaks large amounts of data into smaller packets, while ensuring end-to-end delivery without loss of any data.

### TCP/IP

**Transmission Control Protocol/Internet Protocol**

</br>
<p align="center">
	<a href="https://medium.com/@kamlesh140501/understanding-tcp-ip-the-hackers-guide-to-mastering-the-network-5dc60ec36249">
	<img src="assets/tcp-ip.png" height=200 alt="tcp_ip_schema">
	</a>
</p>
</br>

Its a set of rules that guide and allow computers to communicate on a network such as the internet.

The difference between TCP and IP is that those are two separate computer network protocols. **IP** is the part that obtains the address which the data is sent to, while **TCP** is the part that is responsible for data delivery once that IP address has been found.

Its job is to divide the different communication tasks into layers where each layers have a different function. The data goes through **four individual layers** before it's received on the other end. Then, it goes throught these layers in reverse to reassemble the data and represent it to the recipient.

The four layers are:

- **Datalink Layer / Physical layer**: handles the physical parts of sending and receiving data using the wifi, ethernet, wireless lan...

- **Network Layer**: controls the movement of the packets around the internet.

- **Transport Layer**: provides a reliable data connection between two devices. It divides the data into packets, knows the packets that are received from the other device, and makes sure that the other device knows the packets it receives.

- **Aplication Layer**: it's the group of the application that requires a network communication, which is what the user typically interacts with (like messaging, emails, see a picture or ads).


### Subnet masks

</br>
<p align="center">
	<img src="assets/ip.png" height=100 alt="ip">
</p>
</br>

A subnet mask is a 32 bits (4 bytes) address used to distinguish between a network address and a host address in the IP address. It defines the range of IP addresses that can be used within a network or a subnet.\
So its a network inside a network. It make networks more efficient.

### Default gateways

### Routers and switches

### OSI layers

### Routers

### Switches

---

## 📚 Resources

### General documentation
| Resource | Description |
| :------: | :---------: |
| [Github of lpaube](https://github.com/lpaube/NetPractice) | General explanations of the project |
| [Medium - NetPractice Guide](https://medium.com/@imyzf/netpractice-2d2b39b6cf0a) | General explanations of the project |

### Documentation TCP/IP addressing
| Resource | Description |
| :------: | :---------: |
| [IBM](https://www.ibm.com/docs/en/aix/7.3.0?topic=protocol-tcpip-addressing) | Brief topic of what is TCP/IP addressing |
| [Fortinet (french)](https://www.fortinet.com/fr/resources/cyberglossary/tcp-ip) | Explanation |

### Ipv4 / Ipv6
| Resource | Description |
| [AVG - Difference between Ipv4/Ipv6 (french)](https://www.avg.com/fr/signal/ipv4-vs-ipv6) | Difference between Ipv4 and Ipv6 protocol |

### IA was use to:
- todo

---
