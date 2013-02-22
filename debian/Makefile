#!/usr/bin/make -f


PROJDIR := ..

all:
	$(MAKE) -j4 -C ../cpp/build/linux

clean:
	$(MAKE) -C ../cpp/build/linux clean

install:
	install -d $(DESTDIR)/etc/openzwave
	install -d $(DESTDIR)/usr/include/openzwave
	install -d $(DESTDIR)/usr/include/openzwave/command_classes
	install -d $(DESTDIR)/usr/include/openzwave/value_classes
	install -d $(DESTDIR)/usr/include/openzwave/platform
	install -d $(DESTDIR)/usr/include/openzwave/platform/unix
	install -d $(DESTDIR)/usr/share/openzwave
	install -d $(DESTDIR)/usr/lib
	cp -r $(PROJDIR)/config $(DESTDIR)/usr/share/openzwave
	install $(PROJDIR)/cpp/lib/linux/libopenzwave.so $(DESTDIR)/usr/lib
	install $(PROJDIR)/cpp/lib/linux/libopenzwave.a $(DESTDIR)/usr/lib
	cp -r $(PROJDIR)/cpp/src/*.h $(DESTDIR)/usr/include/openzwave
	cp -r $(PROJDIR)/cpp/src/value_classes/*.h $(DESTDIR)/usr/include/openzwave/value_classes
	cp -r $(PROJDIR)/cpp/src/command_classes/*.h $(DESTDIR)/usr/include/openzwave/command_classes
	cp -r $(PROJDIR)/cpp/src/platform/*.h $(DESTDIR)/usr/include/openzwave/platform
	cp -r $(PROJDIR)/cpp/src/platform/unix/*.h $(DESTDIR)/usr/include/openzwave/platform/unix
