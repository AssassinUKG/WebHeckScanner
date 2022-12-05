# WebHeckScanner (v2.0)
Written by [Graham Zemel](https://grahamzemel.com), using Nikto, Nuclei, Sqlmap, Anew, Gau, and more!

This is a Bash script designed to scan web apps for vulnerabilities using advanced tools while maintaining efficiency  

# Installation
### You must install and configure your directory as I have done or change the code if you have tools in your path already
```
git clone https://github.com/grahamzemel/WebHeckScanner

cd WebHeckScanner
```
Make sure all tools are installed before continuing
```
chmod +x webHeck.sh

sudo ./webHeck.sh -n 'folder name to store results in' -u 'any url(keep the apostrophes)'
```
Note: Upon running this command with the same -n value, or name, it will delete the previous test.

If there are any permission errors running the tool files, run ```chmod +x ${toolfile}``` or ```sudo chmod +x ${toolfile}```.  
If there are any errors with the file system or installing, make sure the directory tree matches the one below.  
# Tools Utilized:
### Larger tools stored in their own folders:

[Sqlmap](https://github.com/sqlmapproject/sqlmap), a tool for testing SQL injection vulnerabilities which are some of the most dangerous.  
[Nikto](https://github.com/sullo/nikto), a tool for scanning websites written in perl, easy to use, one of my favorites.  
[Nuclei](https://github.com/projectdiscovery/nuclei) is likely the most customizable tool out there for web pentesting,
there's about a million different templates to scan with on Github.  

### Solo files, small tools that are contained in 'req_solos/':  

[Anew](https://github.com/tomnomnom/anew): File I/O modification through terminal.    
[Gauplus](https://github.com/bp0lr/gauplus): 'Get All Urls Plus', outdated but still has useful properties.  
[Gau](https://github.com/lc/gau): 'Get All Urls', similar to Subdomainer but I like this tool better.    
[Httpx](https://github.com/projectdiscovery/httpx): Runs a bunch of probes for vulnerabilities, commonly used in combination with most of these tools.  
[PV](https://github.com/a-j-wood/pv): 'Pipe Viewer', used by some of these tools to print the status of a current scan/process.  
[WayBackUrls](https://github.com/tomnomnom/waybackurls): Neat tool that integrates the waybackmachine as a means of fetching old and possibly useful files that may contain credentials or source code.  

# Directory Tree Graph  
WebHeckScanner  
-README.md  
-webHeck.sh  
-nikto/  
-nuclei/  
--nuclei  
-sqlmap/  
-req_solos/  
--anew  
--gau  
--gauplus  
--httpx  
--pv  
--waybackurls  
