# Copyright (C) 2022 Richard Hughes <richard@hughsie.com>

VENDOR=caldigit
PROJECT_NAME=ts4
VERSION=122021
OBJECTS=						\
	TS4-combind-122021-secure-Cus-08.bin		\
	com.caldigit.ts4.pd.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: com.caldigit.ts4.pd.metainfo.xml
	appstream-util validate-relax $<

%.cab: $(OBJECTS)
	gcab --create --nopath $@ $(OBJECTS)
