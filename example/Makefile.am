#######################################
# The list of executables we are building seperated by spaces
# the 'bin_' indicates that these build products will be installed
# in the $(bindir) directory. For example /usr/bin
#bin_PROGRAMS=exampleProgram

# Because a.out is only a sample program we don't want it to be installed.
# The 'noinst_' prefix indicates that the following targets are not to be
# installed.
noinst_PROGRAMS=server client

#######################################
# Build information for each executable. The variable name is derived
# by use the name of the executable with each non alpha-numeric character is
# replaced by '_'. So a.out becomes a_out and the appropriate suffex added.
# '_SOURCES' for example.

# Sources for the a.out 
server_SOURCES= server.c

# Linker options for a.out
server_LDFLAGS = $(LIBEV_LIBS) -lm $(top_srcdir)/src/libjsonrpcc.la
if MINGW32
server_LDFLAGS += -lws2_32 -pthread
endif


# Compiler options for a.out
server_CPPFLAGS = $(LIBEV_CFLAGS) -std=c99 -I$(top_srcdir)/include

# Sources for the client example
client_SOURCES= client.c

# Linker options for client
client_LDFLAGS = $(LIBEV_LIBS) -lm $(top_srcdir)/src/libjsonrpcc.la
if MINGW32
client_LDFLAGS += -lws2_32 -pthread
endif


# Compiler options for client
client_CPPFLAGS = $(LIBEV_CFLAGS) -std=c99 -I$(top_srcdir)/include
