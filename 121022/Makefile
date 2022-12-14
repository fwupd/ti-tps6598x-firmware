# Copyright (C) 2022 Richard Hughes <richard@hughsie.com>

VENDOR=CalDigit
VERSION=TS4-combind-121022-secure-Cus-37
OBJECTS=$(VERSION).bin com.caldigit.ts4.pd.metainfo.xml

all: $(VENDOR)-$(VERSION).cab

clean:
	rm *.cab

check: com.caldigit.ts4.pd.metainfo.xml
	appstream-util validate-relax $<

%.cab: $(OBJECTS)
	gcab --create --nopath $@ $(OBJECTS)
