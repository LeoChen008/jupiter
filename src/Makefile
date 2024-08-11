all: jupiter

CFLAGS = -g -O0

jupiter: main.c
	$(CC) $(CPPFLAGS) $(CFLAGS) -o $@ main.c
check: all
	./jupiter | grep "Hello from .*jupiter!"
	@echo "*** ALL TESTS PASSED ***"

install:
	install -d $(DESTDIR)$(bindir)
	install -m 0755 jupiter $(DESTDIR)$(bindir)

uninstall:
	rm -f $(DESTDIR)$(bindir)/jupiter
	-rmdir $(DESTDIR)$(bindir) > /dev/null 2>&1
clean:
	-rm jupiter
.PHONY: all clean check install uninstall
