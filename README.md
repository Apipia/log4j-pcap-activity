# log4j-pcap-activity
A fun activity using a packet capture file from the log4j exploit (CVE-2021-44228)

## Instructions
Open wireshark and import the PCAP located in this repository: [log4j-exploit.pcap](https://github.com/Apipia/log4j-pcap-activity/blob/main/log4j-exploit.pcap).   
Looking at the packets, answer the following questions.

## Questions

### Easy
1. **Which Packet numbers contain a TCP 3-way-handshake?**.  
_hint: There are 9 of them._

2. **For the first handshake, which server ip and port is establishing a connection with which other server ip and port?**  

3. **For the second?**

4. **What service is associated with the destination port?**

5. **For the third?**  

6. **Looking at the first 4 packets, what can we determine is the type of service running on 172.14.141.132:8080?**

7. **Looking at the 4th packet, what header contains the payload for Log4shell (CVE-2021-44228)?**

8. **Looking at the first 4 packets, what is the first step of the exploit?**

9. **Which packet contains the reply to packet 4?**

### Hard
1. **What is the ip-address of the vulnerable server? What is the ip-address of the attacking machine?**

2. **After recieving the initial payload in packet 4 and recieving the ACK packet, packet 5, what action does the vulnerable server take next?**

3. **Which packet from the attacking machine contains the information to redirect the vulnerable server?**

4. **Looking at this same packet, what is the name of the javaClass we are loading?**

5. **What is the name of the javaFactory?**

6. **What does the vulnerable server do next? (Starting at packet 18)**

8. **What packet contains the RCE that is sent to the server?**

9. **Looking at this packet's 'data', what might be the RCE command sent to the vulnerable server?**

10. **What is the order of establishing and finishing connections with the services and ports on each machine?**

11. **What type of service is running on each of the following ports**:
  -  172.16.141.132:8080
  
  -  172.16.141.131:1389
  
  -  172.16.141.131:8180


### Summary
Now that you have answered the above questions, summarize the steps of the exploit takes as it runs.
ex. First, a http request is sent to the server containing...
