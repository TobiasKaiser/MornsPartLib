all: MornsPMIC.lib MornsVLSDigi.lib MornsDisplays.lib MornsModules.lib
.PHONY: all

MornsPMIC.lib: PMIC_src/lm1117.csv PMIC_src/tps61020.csv PMIC_src/drv8838.csv PMIC_src/spx29302.csv PMIC_src/tps54531.csv PMIC_src/spu03.csv PMIC_src/lt3082.csv
	kipart --overwrite -o $@ $^ 

MornsModules.lib: Modules_src/TE0725-100-2I9.csv Modules_src/NHD-C12864A1Z-FSW-FBW-HTT.csv
	kipart --overwrite -o $@ $^ 

MornsDisplays.lib: Displays_src/VIM-878.csv Displays_src/WS2812B.csv
	kipart --overwrite -o $@ $^ 

#  VLSDigi_src/ATtiny861-20MU.csv => using atmel library instead

MornsVLSDigi.lib: VLSDigi_src/STM32F411xCxE.csv VLSDigi_src/PCF85176T.csv VLSDigi_src/AM26LV32.csv VLSDigi_src/ADS8028.csv VLSDigi_src/Si8621.csv VLSDigi_src/SN74AXC8T245.csv VLSDigi_src/ISL81485.csv
	kipart --overwrite -o $@ $^

.PHONY: clean
clean:
	rm -rf MornsPMIC.lib MornsVLSDigi.lib MornsDisplays.lib
