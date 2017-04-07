all: MornsPMIC.lib MornsVLSDigi.lib
.PHONY: all

MornsPMIC.lib: PMIC_src/lm1117.csv PMIC_src/tps61020.csv
	kipart --overwrite -o $@ $^ 

MornsVLSDigi.lib: VLSDigi_src/STM32F411xCxE.csv VLSDigi_src/ATtiny861.csv
	kipart --overwrite -o $@ $^ 

.PHONY: clean
clean:
	rm -rf MornsPMIC.lib MornsVLSDigi.lib
