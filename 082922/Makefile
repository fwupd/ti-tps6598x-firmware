# Copyright (C) 2022 Richard Hughes <richard@hughsie.com>

VENDOR=caldigit
PROJECT_NAME=ts4
VERSION=082922
OBJECTS=						\
	TS4-combind-082922-secure-Cus-33.bin		\
	com.caldigit.ts4.pd.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: com.caldigit.ts4.pd.metainfo.xml
	appstream-util validate-relax $<

%.cab: $(OBJECTS)
	gcab --create --nopath $@ $(OBJECTS)
