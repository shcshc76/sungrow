Alles zum Thema sungrow PV

### HowTo

Sungrow Wechselrichter und deren Komponenten sind über Modbus TCP abrufbar. Den Wechselrichter selbst bindet man am besten über Ethernet an, 
da der mitgelieferte WLAN Stick nicht gerade stabil läuft und auch die Daten in die Cloud sendet. Die Wallbox ist leider nur über den Wifi-Stick 
erreichbar.

### Updates

Alle updates können über den Winet-S lokal initiiert werden (z.B. mit dem Browser). Voraussetzung ist, dass man die Firmware heruntergeladen hat.
Dazu muss man sich als admin einloggen, die Komponente auswählen und die Firmware hochladen.

![Logo](pics/Sungrow-pic001.png)

Firmware

![Logo](pics/Sungrow-pic002.png)

### Kennwörter

#### Winet-S

Benuter: admin   
Password: pw8888   

Benutzer: user   
Password: pw1111   

### Modbus with Inverter + Wallbox
You can not connect to SHXX-RT + Wallbox with one Modbus connection. You should use two Modbus instances to connect to Inverter and Wallbox. Each separate.
Use for first connection (SHxx-RT) the LAN-Port of Inverter.
The second connection should be the Winet-S Adapter (you can use Wifi or LAN) for Wallbox Modbus.
Don´t pull the Modbus of Winet-S too much. Stable data intervals will be 10 sec. The Inverter Modbus is stable with intervals <= 500ms.
You must set the right "Forwarding Modbus ID" for each device! 
![Logo](pics/bus-id.png)

## Example of Network connection
![Logo](pics/Network.png)


### Ports

![Logo](pics/Inverter_LAN_ports.drawio.svg)
![Logo](pics/overview_modbus_connection.drawio.svg)



### Links:

https://forum.iobroker.net/topic/38441/sungrow-wr-sgh10rt-erfolgreich-mit-modbus-eingebunden

https://forum.iobroker.net/topic/73087/sungrow-wallbox-ac011e-01-erfolgreich-mit-modbus-eingebunden

[photovoltaikforum](https://www.photovoltaikforum.com/thread/166134-daten-lesen-vom-sungrow-wechselrichtern-modbus/)

[Firmware Updates](https://github.com/sungrow-firmware/firmware)

[Modbus Proxy](https://github.com/tiagocoutinho/modbus-proxy)

[iobroker und modbus](https://noegel.io/posts/2022-10-09-sungrow/)
