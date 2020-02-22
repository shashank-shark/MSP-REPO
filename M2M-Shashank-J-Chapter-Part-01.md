# **Hands on M2M Communications**
## Chapter - 01

----
## About
I am writing this tutorial exclusively for Microsoft Student Partner Community and the hackers out there who have a craze on building things from scratch. The tutorial mainly deals with M2M (Machine-to-Machine) communications. The information about the hardware used in this tutorial is given accordingly whenever they are used.

If you find any errors or doubts within this tutorial, then you can reach out to me at :

**email**:  `www.shashankreddy@gmail.com`

**LinkedIn**: ` www.linkedin.com/in/shashank-j-459640151`

## **TOC**
| SNO  |  TITLE | PAGE NO.  |
|---|---|---|
| **1**  | **What are we planning to do ?**  | 1  |
| **2**  | **Let's get started**  | 2  |

# What are we planning to do ?
In the tutorial we will be walking through getting data from **NodeMCU (ESP8266 Wi-Fi SoC)** which acts as publisher and a C running on your computer which acts as subscriber. (PUB-SUB pattern).

*Publisher-Subscriber* is one of the most basic and important type of M2M communication pattern. The *Publisher* publishes different topics depending on the 

I am planning to use **ZeroMQ** (socket library) in this tutorial. You are free to use any library of your interest but the concept and communication patterns remains the same. So let's get started in the next section.

# Let's get started

### **1.** Installing the zeromq library.
In this tutorial I will be using zeromq version 3.2.5 (you are free to use any 3.x.x version) and note that I will be using linux based distros in all my tutorials. If you are a windows user you can install **Ubuntu - Windows Subsystem for Linux (WSL)** from Windows Store. Let's get started.

**Step 1:** Get the source code from the git. Open your terminal and enter these commands.

```sh
$ sudo apt-get update
```

```sh
$ sudo apt-get install -y git build-essential libtoolpkg-config autotools-dev autoconf automake cmake uuid-dev libpcre3-dev libsodium-dev valgrind

$ wget https://github.com/zeromq/zeromq3-x/releases/download/v3.2.5/zeromq-3.2.5.zip

$ unzip zeromq-3.2.5.zip

$ cd zeromq-3.2.5/

$ ./autogen.sh

$ ./configure

$ make check

$ sudo make install

$ sudo ldconfig
```


