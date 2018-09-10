Chrysler, Jeep, and Dodge use Mini50 unsealed 12-circuit (12CKT) Molex connectors.
The Vertical Header (VHDR) is the part that the car's canbus connects to. It's this part: https://www.digikey.com/product-detail/en/molex-llc/0348250124/WM10326-ND/4504599
with this set of dimentions: https://www.molex.com/pdm_docs/sd/348250124_sd.pdf

Going to the stock-LKAS camera is a receptacle (CONN RCPT) which has the same dimensions as the vertical header.
This is the receptacle: https://www.digikey.com/product-detail/en/molex-llc/0348240124/WM10324-ND/4504597
and you'll need these crimp terminals to put wires (or headers) into the receptacle: https://www.molex.com/molex/products/datasheet.jsp?part=active/5600230448_CRIMP_TERMINALS.xml
The receptacle does not have any post holes, but I left them in the PCB design so I could reuse the same part in Eagle as the header.

The work is based on a Chrysler Pacifica Hybrid 2017, although others appear to be the same.

Here is the pin-out for the forward-facing camera as supplied by Mopar (Chrysler): http://connectors.dcctools.com/details.htm?id=203000

Parts list (BOM)
* RJ45 jack for future EON/Pandas that use RJ45 instead of OBD2: RJ45-RA	A-2004-2-4-LPS-N-R	1	https://www.digikey.com/product-detail/en/assmann-wsw-components/A-2004-2-4-LPS-N-R/AE10387-ND/2183638
* Power barrel connector to provide 12V from your Comma Power (can avoid this by wiring IGN to 12V and not using Comma Power): 3-pin	EJ508A	1	https://www.digikey.com/products/en?keywords=ej508a
* Switch to choose stock camera signals: SMD	204-214ST	1 https://www.digikey.com/product-detail/en/cts-electrocomponents/204-214ST/CT204214ST-ND/267313
* OBD2 connector for the Panda to plug in: 16-pin	OBDII-FEMALE	1	https://cn1514770021qfbj.en.alibaba.com/product/60598699808-804284542/J1962F_OBD2_16_Pin_Female_connector_OBD2_Socket.html
* 6 or more headers to build with the mini50 receptacle: https://www.digikey.com/products/en?keywords=S1011EC-40-ND
* Mini50 vertical header: Molex 0348250124 WM10326-ND https://www.digikey.com/product-detail/en/molex-llc/0348250124/WM10326-ND/4504599
* Mini50 receptacle: Molex 0348240124 WM10324-ND https://www.digikey.com/product-detail/en/molex-llc/0348240124/WM10324-ND/4504597
* 6 or more Mini50 terminal connectors to put the headers into the receptacle: Molex 5600230448 WM16315CT-ND https://www.digikey.com/product-detail/en/molex-llc/5600230448/WM16315CT-ND/6702303
