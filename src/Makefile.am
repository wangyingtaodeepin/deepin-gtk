bin_PROGRAMS = exampleapp 

exampleapp_CPPFLAGS = $(GTK_CFLAGS)

exampleapp_LDFLAGS = $(GTK_LIBS)

exampleapp_SOURCES =                       \
	main.c                             \
	exampleapp.c exampleapp.h          \
        exampleappwin.c exampleappwin.h    \
        resources.c

BUILT_SOURCES = resources.c

resources.c: exampleapp.gresource.xml window.ui
	glib-compile-resources $(srcdir)/exampleapp.gresource.xml \
		--target=$@ --sourcedir=$(srcdir) --generate-source

EXTRA_DIST = 					\
	window.ui 				\
	exampleapp.gresource.xml
