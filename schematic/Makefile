all: MornsPMIC.lib MornsVLSDigi.lib MornsDisplays.lib MornsModules.lib
.PHONY: all

MornsPMIC.lib: PMIC_src/lm1117.csv PMIC_src/tps61020.csv PMIC_src/mic706.csv
	kipart --overwrite -o $@ $^ 

MornsModules.lib: Modules_src/TE0725-100-2I9.csv Modules_src/NHD-C12864A1Z-FSW-FBW-HTT.csv
	kipart --overwrite -o $@ $^ 

MornsDisplays.lib: Displays_src/VIM-878.csv
	kipart --overwrite -o $@ $^ 

#  VLSDigi_src/ATtiny861-20MU.csv => using atmel library instead

MornsVLSDigi.lib: VLSDigi_src/STM32F411xCxE.csv VLSDigi_src/PCF85176T.csv VLSDigi_src/AM26LV32.csv VLSDigi_src/ADS8028.csv
	kipart --overwrite -o $@ $^

.PHONY: clean
clean:
	rm -rf MornsPMIC.lib MornsVLSDigi.lib MornsDisplays.lib
