Chrysler, Jeep, and Dodge use Mini50 unsealed 12-circuit (12CKT) Molex connectors.
The Vertical Header (VHDR) is the part that the car's canbus connects to. It's this part: https://www.digikey.com/product-detail/en/molex-llc/0348250124/WM10326-ND/4504599
with this set of dimentions: https://www.molex.com/pdm_docs/sd/348250124_sd.pdf

Going to the stock-LKAS camera is a receptacle (CONN RCPT) which has the same dimensions as the vertical header.
This is the receptacle: https://www.digikey.com/product-detail/en/molex-llc/0348240124/WM10324-ND/4504597
and you'll need these crimp terminals to put wires (or headers) into the receptacle: https://www.molex.com/molex/products/datasheet.jsp?part=active/5600230448_CRIMP_TERMINALS.xml
The receptacle does not have any post holes, but I left them in the PCB design so I could reuse the same part in Eagle as the header.

The work is based on a Chrysler Pacifica Hybrid 2017, although others appear to be the same.

Here is the pin-out for the forward-facing camera as supplied by Mopar (Chrysler): http://connectors.dcctools.com/details.htm?id=203000

## Parts list (BOM)
* RJ45 jack for future EON/Pandas that use RJ45 instead of OBD2: RJ45-RA	A-2004-2-4-LPS-N-R	1	https://www.digikey.com/product-detail/en/assmann-wsw-components/A-2004-2-4-LPS-N-R/AE10387-ND/2183638
* Power barrel connector to provide 12V from your Comma Power (can avoid this by wiring IGN to 12V and not using Comma Power): 3-pin	EJ508A	1	https://www.digikey.com/products/en?keywords=ej508a
* Switch to choose stock camera signals: SMD	204-214ST	1 https://www.digikey.com/product-detail/en/cts-electrocomponents/204-214ST/CT204214ST-ND/267313
* OBD2 connector for the Panda to plug in: 16-pin	OBDII-FEMALE	1	https://cn1514770021qfbj.en.alibaba.com/product/60598699808-804284542/J1962F_OBD2_16_Pin_Female_connector_OBD2_Socket.html
* 6 or more generic headers or stiff wire that will go in the terminals: https://www.digikey.com/products/en?keywords=S1011EC-40-ND (This linked item is 40 headers together, so you only need to buy one.)
* Mini50 vertical header: Molex 0348250124 WM10326-ND https://www.digikey.com/product-detail/en/molex-llc/0348250124/WM10326-ND/4504599
* Mini50 receptacle: Molex 0348240124 WM10324-ND https://www.digikey.com/product-detail/en/molex-llc/0348240124/WM10324-ND/4504597
  * If out of stock, the bridge version will work but won't sit flush on the PCB: 0348241124 https://www.digikey.com/product-detail/en/molex-llc/0348241124/WM13165-ND/4693133
* 6 or more Mini50 terminal connectors to put the headers into the receptacle: Molex 5600230448 WM16315CT-ND https://www.digikey.com/product-detail/en/molex-llc/5600230448/WM16315CT-ND/6702303
  * There are several different types of terminals. Pretty much any of them should work. The sizes are for different gage of wires: L for 0.35mm2, M for 0.22mm2, S for 0.13mm2. The linked headers are 0.41mm2, so get the L size, which is what I've linked to here.

## Troubleshooting

If you get a wire incorrect and the car starts faulting, typically removing your hardware and then turning the car off and back on again will fix it. If you can't turn the car off, such as due to faulting the shifter, then there are fuses located in the engine compartment, under the battery's black plastic cover. Carefully pull the fuse, check if it's blown and replace it. Warning: electricity can kill or injure you, refer to your car's service manual. The map for which fuse is which is located on the inside of the black plastic cover that you need to remove to access the fuses. Try removing and replacing these fuses to reboot the car (for 2017 pacifica hybrid):
- F78 is blue 15A (shifter)
- F57 (PIM - Main Power Supply)
- F62 (PIM - Redundant Main Power Supply)
