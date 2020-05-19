DESTDIR := ""
PREFIX := /usr/local

.PHONY: build
build: electric-alibi

.PHONY: install
install: build
	mkdir -p ${DESTDIR}${PREFIX}/bin
	cp electric-alibi ${DESTDIR}${PREFIX}/bin/electric-alibi

.PHONY: clean
clean:
	rm -f electric-alibi

electric-alibi: electric-alibi.c
	gcc -I${PROTON_BUILD}/c/include -o $@ $< ${PROTON_BUILD}/c/libqpid-proton-core-static.a ${PROTON_BUILD}/c/libqpid-proton-proactor-static.a
#	gcc $< -o $@ -static -I${PROTON_BUILD}/c/include -L${PROTON_BUILD}/c -lqpid-proton-core-static -lqpid-proton-proactor-static

# gcc -Wall -static -I/opt/gdbm-1.8.3/include/
#    -L/opt/gdbm-1.8.3/lib/ dbmain.c -lgdbm
