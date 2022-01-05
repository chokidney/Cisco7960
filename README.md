# Cisco7960
Cisco7960 Setup with FreePBX

# This file to instruction to setup Cisco 7960 on FreePX, including some errors that I had and solved.

===================================
Problem: Protocol Application Invalid
  Can happen after factory reset
  Solution: Go to **pfSense** to set up TFTP server  > DHCP Server > LAN
     TFTP Server <==  put FreePBX address here where TFTP server is located at
     * if you set up this one, no need to setup phone for Alternative TFTP (as it is already done)

7960/7940 Setup
Setting => Unlock => Password = cisco
   Network configuration > 32 Alternate TFTP: YES

=======================================
Problem: Phone Unprovisioned continues:
   Go to Cisco7960 Network Configuration => GARP change to "NO"
