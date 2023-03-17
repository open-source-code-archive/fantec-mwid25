
ZIP=FANTEC_MWiD25_Firmware_20131009-v2.000.030.zip


all:
	@if [ -f $(ZIP) ]; then make split; else make zip; fi

split:
	split --verbose --bytes 50M -d --suffix-length=1 $(ZIP) $(ZIP).part-

zip:
	cat $(ZIP).part-* > $(ZIP)

clean:
	@rm -vf $(ZIP).part-*

