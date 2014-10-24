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
Internet | ip a(eerst install net-tool) , Nat = 10.0.2.15 in VBox, default gateway(ip r) 
Transport |
Applicatie |

    
    

