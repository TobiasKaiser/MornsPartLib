all: MornsPMIC.lib MornsVLSDigi.lib MornsDisplays.lib
.PHONY: all

MornsPMIC.lib: PMIC_src/lm1117.csv PMIC_src/tps61020.csv
	kipart --overwrite -o $@ $^ 

MornsDisplays.lib: Displays_src/VIM-878.csv
	kipart --overwrite -o $@ $^ 

MornsVLSDigi.lib: VLSDigi_src/STM32F411xCxE.csv VLSDigi_src/ATtiny861.csv
	kipart --overwrite -o $@ $^2 

.PHONY: clean
clean:
	rm -rf MornsPMIC.lib MornsVLSDigi.lib
