**সব কাজ সঠিকভাবে করার জন্য আগে server ঠিক করে নিন:**
```
echo "nameserver 8.8.8.8" > /etc/resolv.conf
```
```
apt update --allow-releaseinfo-change

```
 



**Basic Tools Install**



```
sudo apt install coreutils npm php php-common php-cli php-curl php-gd php-mysql curl git wget -y

```

# 📋 Tools Description 
<hr>
</br>
</br>

## Coding & Programing

**Termux এ html, css, c programing, c++, java, javascript রান করতে প্রয়োজন।**


```
sudo apt install build-essential clang nodejs default-jdk nano -y

```

**(C)রান:** `gcc file.c -o file` লিখে এন্টার দিন, তারপর `./file` দিয়ে রান করুন।


**(C++)রান:** `g++ file.cpp -o file` লিখে এন্টার দিন, তারপর `./file` দিয়ে রান করুন।

**(javascript)রান:** সরাসরি `node file.js` লিখে এন্টার দিন।

**(java)রান:** `javac Main.java` দিয়ে কম্পাইল করে `java Main` লিখে রান করুন।

**(html/css)রান:** প্রথমে আপনার ফাইলটি যে ফোল্ডারে আছে, সেখানে পাইথন সার্ভারটি চালু করুন `python3 -m http.server 8000` এবার ব্রাউজারে `http://localhost:8000` লিখে সার্চ করুন।(python3 install থাকতে হবে)


</br>
</br>


## Ruby
**এটি একটি ডাইনামিক প্রোগ্রামিং ল্যাঙ্গুয়েজ, যা Metasploit-এর মতো বিভিন্ন সিকিউরিটি ফ্রেমওয়ার্ক চালানোর জন্য প্রয়োজন।**

## ১. Ruby Setup
Ruby এবং এর প্যাকেজ ম্যানেজার (Gem) সেটআপ করতে নিচের কমান্ডটি দিন:
```
sudo apt install ruby ruby-dev -y

```
## ২. Ruby Gems
Ruby-র বিভিন্ন লাইব্রেরি বা 'Gems' ইনস্টল করার জন্য এটি প্রয়োজন হয়:
```
sudo gem install bundler

```
আপনি যদি কোনো নির্দিষ্ট Ruby স্ক্রিপ্ট (.rb ফাইল) চালাতে চান, তবে কমান্ডটি হবে:

`ruby [ফাইলের_নাম].rb`

</br>
</br>


## Port Forwarding (openssh & cloudflared)

**রিমোট সার্ভারের সাথে নিরাপদভাবে কানেক্ট হওয়া এবং একটি টানেল তৈরি করা যা আপনার লোকাল সার্ভিসকে ইন্টারনেটে ছড়িয়ে দিবে।**
## Linux
```
apt install openssh-server -y && wget https://github.com/cyber99aams/linux-master-setup/releases/download/v4.0/cloudflared-linux-arm64 && chmod +x cloudflared-linux-arm64 && mv cloudflared-linux-arm64 /usr/local/bin/cloudflared && cloudflared --version



```
## Termux
```
pkg install openssh -y && wget https://github.com/cyber99aams/linux-master-setup/releases/download/v4.0/cloudflared-linux-arm64 && chmod +x cloudflared-linux-arm64 && mv cloudflared-linux-arm64 $PREFIX/bin/cloudflared && cloudflared --version

```
Cloudflared দিয়ে লিঙ্ক পাবলিশ করা (নতুন টার্মিনাল সেশনে) 

`cloudflared tunnel --url http://localhost:8080`

</br>
</br>


## Python

**স্ক্রিপ্টিং, অটোমেশন এবং সাইবার সিকিউরিটির বেশিরভাগ টুলস রান করার জন্য এটি সবচেয়ে গুরুত্বপূর্ণ ল্যাঙ্গুয়েজ।**

### ১. python Core Setup
​আপনার সিস্টেমে Python-এর মূল ফাইল এবং প্যাকেজ ম্যানেজার (pip) ইনস্টল করতে এই কমান্ডটি দিন:
```
sudo apt install python3 python3-pip python3-dev -y

```
### ২. Environment Setup
​আধুনিক লিনাক্স সিস্টেমে পাইথন লাইব্রেরিগুলো আলাদাভাবে ম্যানেজ করার জন্য venv প্রয়োজন হয়। এটি সেটআপ করতে:
```
sudo apt install python3-venv -y

```
## ৩. Normal Hacking Library
​পাইথন ভিত্তিক টুলগুলো চালানোর সময় যেন কোনো এরর না আসে, সেজন্য নিচের কমান্ড দিয়ে প্রয়োজনীয় লাইব্রেরিগুলো একবারেই সেটআপ করে নিন:
```
pip3 install requests colorama bs4 scapy --break-system-packages

```
দ্রষ্টব্য: আপনি যদি Kali Linux-এর লেটেস্ট ভার্সন ব্যবহার করেন, তবে শেষে --break-system-packages যোগ করা জরুরি, অন্যথায় এরর আসতে পারে।







</br>
</br>







# Information Gathering

## Whois 

**এটি একটি প্রোটোকল বা সার্ভিস যা ইন্টারনেটের যেকোনো ডোমেইন নাম বা আইপি অ্যাড্রেসের মালিকানা সংক্রান্ত তথ্য খুঁজে বের করতে ব্যবহৃত হয়।**
```
sudo apt install whois -y

```
এটি দিয়ে যেকোনো website এর তথ্য দেখতে টাইপ করুন
Website: 

`whois [domain].com`

আর যেকোনো Ip Address এর তথ্য দেখতে টাইপ করুন
IP Address : 

`whois [ip]`

## Maltego
**ইন্টারনেটে ছড়িয়ে থাকা পাবলিক তথ্য ব্যবহার করে কোনো নির্দিষ্ট ব্যক্তি বা প্রতিষ্ঠানের ডিজিটাল কানেকশন বা প্রোফাইল তৈরি করা সম্ভব।**
```
sudo apt install maltego -y

```
## Maigret

**​এটি ইউজারনেম দিয়ে ৩০০০টিরও বেশি ওয়েবসাইট স্ক্যান করে প্রোফাইলের ভেতর থেকে ইমেইল, পূর্ণ নাম এবং অন্যান্য ব্যক্তিগত তথ্যও বের করার চেষ্টা করে।**
```
pip install maigret --break-system-packages

```
ব্যবহার: 

`maigret [username]`

## Holehe

​**এর কাজ হলো শুধুমাত্র একটি Email Address দিয়ে ইন্টারনেটের ১২০টিরও বেশি সাইট (যেমন: Twitter, Instagram, LinkedIn, Netflix, Spotify) চেক করা যে ওই ইমেইল দিয়ে সেখানে কোনো অ্যাকাউন্ট খোলা আছে কি না।**
```
pip3 install holehe

```
ব্যবহার: 

`holehe user@example.com`






</br>
</br>





# Network Scanning 

## Nmap

**এটি একটি শক্তিশালী নেটওয়ার্ক স্ক্যা**নিং এবং সিকিউরিটি অডিটিং টুল যা নেটওয়ার্কের নিরাপত্তা যাচাই করতে ব্যবহৃত হয়।**
```
sudo apt install nmap -y

```
## Shodan 

**ইন্টারনেটে থাকা সিসিটিভি ক্যামেরা, স্মার্ট ফ্রিজ বা কন্ট্রোল সিস্টেমের মতো ডিভাইসগুলো খুঁজে বের করা এবং সেগুলোর দুর্বলতা দেখতে পারে।**
<h3>
<p align="center">
<a href="https://www.shodan.io/">Use In Website</a>
</p>
</h3>

## ১. Shodan Setup
​টার্মিনাল থেকে সরাসরি এটি ব্যবহার করার জন্য এর পাইথন লাইব্রেরি সেটআপ করতে হয়।
```
pip install shodan

```
## Configuration (API Key)
​Shodan ব্যবহার করতে হলে আপনাকে <a href="https://www.shodan.io/">shodan.io</a> থেকে একটি ফ্রি অ্যাকাউন্ট খুলে API Key সংগ্রহ করতে হবে। তারপর নিচের কমান্ডটি দিন:
```
shodan init আপনার_API_KEY

```

## Searchsploit (Exploit Database)
​এর কাজ হলো বিভিন্ন সফটওয়্যার বা সার্ভিসের দুর্বলতা (Vulnerabilities) খুঁজে বের করা।
```
sudo apt install exploitdb -y

```
**ব্যবহার:** ধরুন একটি সার্ভারে Apache 2.4.41 চলছে। Searchsploit-এ গিয়ে সার্চ করলে এটি বলে দেবে এই ভার্সনের জন্য ইন্টারনেটে কোনো তৈরি করা হ্যাকিং স্ক্রিপ্ট বা এক্সপ্লয়েট আছে কি না।

**সার্চ করার নিয়ম:** `searchsploit apache 2.4`






</br>
</br>







# Network Monitoring

## Ettercap

**​এটি মূলত Man-in-the-Middle (MITM) অ্যাটাকের জন্য ব্যবহৃত হয়।**
```
sudo apt install ettercap-graphical -y

```
## Wireshark 

**​এটি আপনার নেটওয়ার্কের ভেতর দিয়ে যাতায়াত করা প্রতিটি ডেটা প্যাকেটকে "ক্যাপচার" করে এবং তা বিস্তারিতভাবে দেখায়।**
```
sudo apt install wireshark -y

```
ইনস্টলেশনের সময় একটি পপ-আপ আসতে পারে যে non-superusers প্যাকেট ক্যাপচার করতে পারবে কি না, সেখানে Yes সিলেক্ট করুন।












</br>
</br>





# Password Cracking 

## John the Ripper (JTR)

**এটি বিভিন্ন ধরনের এনক্রিপ্টেড ফাইল (যেমন: জিপ ফাইল বা লিনাক্স পাসওয়ার্ড ফাইল) ক্র্যাক করতে সক্ষম**
```
sudo apt install john -y

```
## Hydra 

**একটি অত্যন্ত শক্তিশালী লগইন ব্রুট-ফোর্স (Brute-force) টুল। যা বিভিন্ন ধরনের পাসওয়ার্ড ক্রেকিং এর জন্য ব্যবহৃত হয়**
```
sudo apt install build-essential make cmake libcurl4-openssl-dev libssl-dev -y

```
```
git clone https://github.com/cyber99aams/thc-hydra.git
cd thc-hydra
./configure

```

## Aircrack-ng

**আশেপাশের কোনো লক করা ওয়াইফাই নেটওয়ার্কের ডাটা প্যাকেট ক্যাপচার করে সেটির পাসওয়ার্ড ডিক্রিপ্ট করা সম্ভব**
```
sudo apt install aircrack-ng -y

```
**গ্রাফিকাল ইন্টারফেস (শুধুমাত্র PC-র জন্য)
​আপনি যদি কমান্ড লাইনের বদলে উইন্ডো বা GUI ব্যবহার করতে চান (যা পিসিতে সহজ), তবে xhydra ইনস্টল করতে পারেন।**
```
sudo apt install xhydra -y

```
## Hashcat
**​এটি বিশ্বের দ্রুততম পাসওয়ার্ড রিকভারি বা ক্র্যাকিং টুল। এটি মূলত হ্যাশ ফাইল (যেমন: MD5, SHA-1) থেকে আসল পাসওয়ার্ড বের করার জন্য ব্যবহৃত হয়।**
```
sudo apt install hashcat -y
```
## Ophcrack 

**উইন্ডোজ কম্পিউটারের অ্যাডমিন পাসওয়ার্ড ভুলে গেলে তা রিসেট বা উদ্ধার করার জন্য এটি সেরা।**

```
sudo apt install ophcrack -y
```



</br>
</br>





# System Control And Remote Access 

## Metasploit Framework

**এটি পেনিট্রেসন টেস্টিংয়ের জন্য সবথেকে বড় এবং শক্তিশালী ফ্রেমওয়ার্ক।**

## ১. Metasploit Install
মেটাসপ্লয়েট বেশ বড় ফাইল, এটি ইনস্টল করতে কিছুটা সময় এবং স্টোরেজ লাগবে:
```
sudo apt install metasploit-framework -y

```
## ২. Database Connect 

**​(i) Start PostgreSQL Service**

মেটাসপ্লয়েট ডেটাবেস হিসেবে PostgreSQL ব্যবহার করে। এটি চালু করতে লিখুন:
```
service postgresql start

```
**(ii) Database Essentialis**
​প্রথমবার ব্যবহারের সময় ডেটাবেসটি তৈরি করে নিতে হয়:
```
sudo msfdb init

```
দ্রষ্টব্য:Database Connect সুধু root ইউজারদের জন্য।

## ​৩. Start Metasploit 
​এখন মূল ফ্রেমওয়ার্কটি চালু করুন:
```
msfconsole

```





</br>
</br>







# Web & Database Hacking 

## SQLmap 

**কোনো ওয়েবসাইটের ডাটাবেসে ঢুকে ব্যবহারকারীদের নাম, ইমেইল এবং পাসওয়ার্ডের তালিকা বের করে আনা সম্ভব।**
```
sudo apt install sqlmap -y

```
## Burp Suite

**এটি আপনার ব্রাউজার থেকে কোনো ওয়েবসাইটে ডেটা যাওয়ার সময় সেই ডেটাকে মাঝপথে আটকে দেয়। এরপর আপনি চাইলে সেই ডেটা (যেমন: ইউজারনেম, পাসওয়ার্ড বা কুকি) পরিবর্তন করে সার্ভারে পাঠাতে পারেন।**
```
sudo apt install burpsuite -y

```
## OWASP ZAP

**এর কাজ ব্রাউজার এবং সার্ভারের মাঝখানের ট্রাফিক এনালাইসিস করা। তবে এর একটি বিশেষ সুবিধা হলো এর Automated Scanner, যা নিজে থেকেই ওয়েবসাইটের সাধারণ দুর্বলতাগুলো (যেমন: XSS, SQLi) খুঁজে বের করতে পারে**
```
sudo apt install zaproxy -y

```
## Nikto

​**এটি একটি অত্যন্ত শক্তিশালী Web Server Scanner। এর কাজ হলো কোনো ওয়েবসাইটের সার্ভারে কোনো ধরনের সিকিউরিটি হোল, বিপজ্জনক ফাইল বা পুরনো সফটওয়্যার ভার্সন আছে কি না তা খুঁজে বের করা।**
```
sudo apt install nikto -y

```
## BeEF (Browser Exploitation Framework)
**​এর কাজ হলো কোনো ভিক্টিমের ওয়েব ব্রাউজারকে (Chrome, Firefox) হ্যাক করা। একবার যদি ভিক্টিম আপনার তৈরি করা লিঙ্কে ক্লিক করে, তবে আপনি তার ব্রাউজারের মাধ্যমে তার ওয়েবক্যাম দেখা, লোকেশন জানা বা তার সোশ্যাল মিডিয়া কুকি চুরি করার মতো কাজ করতে পারবেন।**
```
sudo apt install beef-xss -y

```








