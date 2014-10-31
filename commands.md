#DNS-server
Troubleshooting van de DNS-server
 
 Functie| Commando
 ----------| -------------------
 Controleren van de DNS instellingen | ```nslookup```
 Vinden van ip-adres van een domein | ```nslookup "naam van domein (bv. yahoo.com)"```
 Reverse domain lookup | ```nslookup "ip-adres"```
 Debug mode enablen | ```nslookup -debug "naam van domein"```
 DNS registreren | ```ipconfig /registerdns```
 DNS instellingen tonen | ```ipconfig /displaydns```
 Poortnummer veranderen van DNS (kan helpen) | ```nslookup -port "poortnummer" "domeinnaam" (vb nslookup -port 54 google.com)```
 DNS instellingen tonen | ```ipconfig /displaydns```
  DNS instellingen tonen | ```ipconfig /displaydns```
   DNS instellingen tonen | ```ipconfig /displaydns```
    DNS instellingen tonen | ```ipconfig /displaydns```
 
 
 
 
 
 
 
 
 
 
#Checklist
Volgorde voor troubleshooten

Laag | Opties
-----------|----------
Hardware | kabels?
Netwerkinterface | ....
Internet | ip a(eerst install net-tool) , Nat = 10.0.2.15 in VBox, default gateway(ip r) , DNS (cat /etc/resolv.conf) ping default gateway, ping andere host binnen subnet, traceroute naar buiten(kan falen), ping DNS,dig installeren, algemeen zoekcommando : yum provides -bin/dig(=PATTERN)
Transport | Zijn de poorten open?: sudo systemctl status httpd.service, sudo ss -tulpn(TcpUdpListenProcessNumber), sudo ps -ef. poort geblokkeerd? sudo firewall -cmdd --list-all, sudo iptables -L -n -v.Van buitenaf:portscanner: nmap -A -T4, nmap -sS -sU, 
Applicatie | Client software of troubleshooting tools : curl,wget voor web, smbclient,nmblookup,net use voor fileserver.Bekijk de logfiles!: sudo journalctl -f -u httpd.service

Foutboodschappen : - No route to host: internetlaag, probleem met IP
                   - Connection refused : transportlaag, service draait niet of is gefilterd..
                   - Unable to resolve host : internet/applicatie, DNS niet beschikbaar
                   - ERROR 404 : applicatie, URL verkeerd, fout in Apache...

    
    

