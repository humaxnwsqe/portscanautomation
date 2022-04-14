# Open Port Scanning Automation
## Purpose
Nmap(https://nmap.org/) is a well-known tool to scan open ports for like home gateway products. This tool is simple to use but result that this tool makes is XML format. XML is not easy to read when it compares to HTML so the results made from Nmap have low readability.
To overcome this inconvenience, I tried to use lxml package to convert XML format to HTML. And windows batch has also been used to remove the other inconvenience to execute Nmap using the combination of multi options like TCP, UDP, IPv4, IPv4, LAN, and WAN. Plus let all HTML converted files send through e-mail to check the results after overnight execution

## Used major technique
- Python 3
- lxml (to convert xml to html)
- Windows batch

## Simple Diagram and Sequences
- Diagram

<p align="center">
    <img src='./images/openportscan_auto_diagram.png'>
    <br>
    
</p>

- Sequences
  - 1st. Execution Nmap with the combination of each option
    - TCP, IPv4, LAN
    - UDP, IPv4, LAN
    - TCP, IPv6, LAN
    - UDP, IPv6, LAN
    - TCP, IPv4, WAN
    - UDP, IPv4, WAN
    - TCP, IPv6, WAN
    - UDP, IPv6, WAN 
  - 2nd. After finishing Nmap executions, the results will be created as XML
  - 3rd. These XML results are going to be converted to HTML using lxml package.
  - 4th. The files converted to HTML will be sent to the target e-mail address using a simple python code. (End)
