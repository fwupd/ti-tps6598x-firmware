# Copyright (C) 2022 Richard Hughes <richard@hughsie.com>

VENDOR=CalDigit
VERSION=TS4-combind-122021-secure-Cus-08
OBJECTS=$(VERSION).bin com.caldigit.ts4.pd.metainfo.xml

all: $(VENDOR)-$(VERSION).cab

clean:
	rm *.cab

check: com.caldigit.ts4.pd.metainfo.xml
	appstream-util validate-relax $<

%.cab: $(OBJECTS)
	gcab --create --nopath $@ $(OBJECTS)
