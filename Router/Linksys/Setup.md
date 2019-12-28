# Linksys Router Setup

**Router Model:** EA6350 | _3.1.10.191322_

Only follow this guide for a new router setup. To factory reset a Linksys hold in the reset button for ~11 seconds and let go (or go to Troubleshooting > Diagnostics > Factory Reset). Also, make sure the computer used to set it up is hardwired! Visit http://192.168.1.1 to access the router.

1. Setup 2.4/5Ghz Wireless access points w/ strong passwords
2. Create a local access account & password
   1. Default password is `admin`
3. Rename the router
4. Disable guest access (Forces weak password!)
5. Media Prioritization
   1. pi-hole
   2. Gaming PC
   3. Macbook Pro
6. External Storage
   1. Enable Secure Folder Access
      1. Create a user with a strong password
      2. Create a shared folder for the new user (e.g Public)
   2. Disable Media Server
7. Wireless
   1. For 2.4 and 5GHz networks:
      1. SSID: Clever, long, simple and unique
      2. Security Mode: WPA2 Personal
      3. Password: Very strong
      4. Disable "Broadcast SSID"
8. Connectivity
   1. Basic
      1. Verify Network Access Points are correct from Step 6
      2. Change Time Zone
   2. Local Network
      1. Change Start IP address
      2. Set Maximum number of users
      3. Set Static DNS:
         1. `192.168.1.2` - pi-hole
         2. `1.1.1.1` - CloudFlare
         3. `1.0.0.1` - CloudFlare 2
         4. `8.8.8.8` - Google
      4. DHCP Reservations: Setup any reserved IPs necessary here (need MAC addresses!)
         1. Tip: To assign out-of-range, you may need to change the range first, assign DHCP, and change the range back

###### Enjoy!
