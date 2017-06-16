# Koruza current consumption:

* 48mA @24V only power supplys and Eth HUB turned on, nothing else is connected.

---


* DCDC 5V
	* power disipation: 1,25W see the power dissipation diagram for [SPM15-050-Q12 model in the datasheet](link1_DCDC5V) (page 11.)
		
* DCDC 9V


* SFP LDO 3V3
	* see the power dissipation diagram in the [data sheet (LM1117, Figure 6.)](link2_1117)

* CM SW 3V3/1V8
	* Power Dissipation: 1.66W

* HUB			 
	* SUSPEND0
		* Supply current (VDD33IO, VDD33A): 74mA
		* Power Dissipation (Device Only): 245mW
		* Power Dissipation (Device and Ethernet components): 379mW
	* SUSPEND1
		* Supply current (VDD33IO, VDD33A): 68mA
		* Power Dissipation (Device Only): 224mW
		* Power Dissipation (Device and Ethernet components): 229mW
	* SUSPEND2
		* Supply current (VDD33IO, VDD33A): 4.2mA
		* Power Dissipation (Device Only): 14mW
		* Power Dissipation (Device and Ethernet components): 14.1mW
	* Operational Current Consumption & Power Dissipation(VDD33IO = VDD33A = 3.3V)
		* 100BASE-TX Full Duplex (USB High-Speed)
			* Supply current (VDD33IO, VDD33A): 231mA
			* Power Dissipation (Device Only): 763mW
		* 10BASE-T Full Duplex (USB High-Speed)
			* Supply current (VDD33IO, VDD33A): 188mA
			* Power Dissipation (Device Only): 621mW
		* 10BASE-T Full Duplex (USB Full-Speed)
			* Supply current (VDD33IO, VDD33A): 152mA
			* Power Dissipation (Device Only): 502mW
	* Magnetic power consumption:
		* 100BASE-TX: ~42mA
		* 10BASE-T: ~104mA

* LED            
* ~3-4mA

* SFP module 1

* SFP module 2

* RPI Camera

* RPI Compute Module
	
  
  [link1_DCDC5V]:  <https://github.com/IRNAS/koruza-compute-module/blob/board_0.2/docs/datasheet/SPM15-050-Q12P-C.pdf>
  [link2_1117]: <https://github.com/IRNAS/koruza-compute-module/blob/board_0.2/docs/datasheet/reg1117.pdf>
  [hardware_workflow]: <Irnas_GitHub_hardware_workflow.md>
