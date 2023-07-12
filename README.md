# About
The MITM implant intercepts .exe and .sh file download requests from the target machine (to the target server) and replaces the file that the target machine intended to download with either bad.exe or bad.sh. Otherwise no other network operations are affected and network traffic is passed along like normal. 

Note: Although the MITM implant uses ARP spoofing, if the implant is killed by a SIGINT being sent, the implant reARPs the targetss. 

# Usage
To use the MITM implant run `./implant.py <target-ip> <server-ip>` where `target-ip` is the ip address of the downloader sending the HTTP request and `server-ip` is the ip address of the server sending the HTTP response (containing the file to be downloaded).