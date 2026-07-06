# Using Splunk to Identify Brute Force Attacks
During the development of my homelab, I took the time to setup Splunkforwader on my Windows 2022 Server. I installed Splunk on my administrator PC. 
I replicated a brute force attack via my Kali Linux machine. This simulated a real-world brute force attack.

Using Splunk allowed me to see in real time the dozens of failed login attempts & the successful login from an unknown IP address. This alerted me that someone outside of the domain had gained access to my server.

Below is a list of event logs that I set alerts for that would trigger upon Splunk receiving them.             
4648 = A logon was attempted using explicit credentials                       
4625 = An account failed to log on                         
4624 = An account was successfully logged on                           

Below is a picture of the real-time logs I was receiving via Splunk that alerted me of the brute force attack

image1.png

