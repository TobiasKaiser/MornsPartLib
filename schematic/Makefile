all: MornsPMIC.lib
.PHONY: all

MornsPMIC.lib: PMIC_src/lm1117.csv PMIC_src/tps61020.csv
	kipart -o $@ $^ 


.PHONY: clean
clean:
	rm -rf MornsPMIC.lib
