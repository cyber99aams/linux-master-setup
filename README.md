**সবকিছু সঠিকভাবে করার জন্য আগে server ঠিক করে নিন:**
```
echo "nameserver 8.8.8.8" > /etc/resolv.conf
```
# 📋 Tools Description 
## Git

**GitHub থেকে বিভিন্ন টুল এবং স্ক্রিপ্ট ক্লোন (ডাউনলোড) করার জন্য এটি অপরিহার্য।**
```
sudo apt install git -y

```
ব্যবহার: কোনো রিপোজিটরি ক্লোন করতে লিখুন: git clone [লিঙ্ক]
## Wget

**ইন্টারনেট থেকে যেকোনো ফাইল সরাসরি টার্মিনালে ডাউনলোড করার জন্য একটি জনপ্রিয় কমান্ড-লাইন টুল**
```
sudo apt install wget -y

```
ব্যবহার: কোনো ফাইল ডাউনলোড করতে লিখুন: wget [ডাওনলোড লিঙ্ক]
## Curl 

**বিভিন্ন প্রোটোকল (যেমন HTTP, FTP) ব্যবহার করে ডাটা ট্রান্সফার এবং API টেস্টিং করার জন্য এটি ব্যবহৃত হয়।**
```
sudo apt install curl -y

```
## OpenSSH & Cloudflared (port forwarding) 

**রিমোট সার্ভারের সাথে নিরাপদভাবে কানেক্ট হওয়া এবং একটি টানেল তৈরি করা যা আপনার লোকাল সার্ভিসকে ইন্টারনেটে ছড়িয়ে দিবে।**
```
wget https://github.com/cyber99aams/linux-master-setup/releases/download/v4.0/cloudflared-linux-arm64
chmod +x cloudflared-linux-arm64
sudo mv cloudflared-linux-arm64 /usr/local/bin/cloudflared
cloudflared --version

```
```
sudo apt install openssh-server git -y            sudo mkdir -p /run/sshd
sudo /usr/sbin/sshd
```
Cloudflared দিয়ে লিঙ্ক পাবলিশ করা (নতুন টার্মিনাল সেশনে) 

`cloudflared tunnel --url http://localhost:8080`



## php 

**লোকাল হোস্ট সার্ভার তৈরি করা এবং সার্ভার-সাইড স্ক্রিপ্টিং প্রজেক্টের জন্য এটি ব্যবহার করা হয়।**

```
sudo apt install php php-common php-cli php-curl php-gd php-mysql -y

```
## nano 

**টার্মিনালের ভেতরে সরাসরি ফাইল এডিট করা বা নতুন স্ক্রিপ্ট লেখার জন্য একটি সহজ টেক্সট এডিটর।**
```
sudo apt install nano -y

```
## nodejs 

**জাভাস্ক্রিপ্ট রানটাইম এনভায়রনমেন্ট, যা বিভিন্ন আধুনিক ওয়েব টুলস এবং সার্ভার অ্যাপ্লিকেশন চালাতে সাহায্য করে।**
```
sudo apt install nodejs npm -y

```
## coreutils 

**ফাইল ম্যানেজমেন্ট এবং টেক্সট প্রসেসিং করার জন্য প্রয়োজনীয় মৌলিক লিনাক্স কমান্ডগুলোর (যেমন: ls, cp, mv) সমষ্টি।** 
```
sudo apt install coreutils -y

```
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


















# Password Cracking 

## John the Ripper (JTR)

**এটি বিভিন্ন ধরনের এনক্রিপ্টেড ফাইল (যেমন: জিপ ফাইল বা লিনাক্স পাসওয়ার্ড ফাইল) ক্র্যাক করতে সক্ষম**
```
sudo apt install john -y

```
## Hydra 

**একটি অত্যন্ত শক্তিশালী লগইন ব্রুট-ফোর্স (Brute-force) টুল। যা বিভিন্ন ধরনের পাসওয়ার্ড ক্রেকিং এর জন্য ব্যবহৃত হয়**
```
sudo apt install hydra -y

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








