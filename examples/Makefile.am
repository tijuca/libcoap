# examples/Makefile.am
#
# Copyright (C) 2015-2018 Carsten Schoenert <c.schoenert@t-online.de>
#
# This file is part of the CoAP C library libcoap. Please see README and
# COPYING for terms of use.

# just do nothing if 'BUILD_EXAMPLES' isn't defined
if BUILD_EXAMPLES

# picking up the default warning CFLAGS into AM_CFLAGS
AM_CFLAGS = -I$(top_builddir)/include -I$(top_srcdir)/include \
            -I$(top_srcdir)/include/coap$(LIBCOAP_API_VERSION) \
            $(WARNING_CFLAGS) $(DTLS_CFLAGS) -std=c99

# etsi_iot_01 and tiny are missing
bin_PROGRAMS = \
 coap-client@LIBCOAP_DTLS_LIB_EXTENSION_NAME@ \
 coap-server@LIBCOAP_DTLS_LIB_EXTENSION_NAME@ \
 coap-rd@LIBCOAP_DTLS_LIB_EXTENSION_NAME@

coap_client@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_SOURCES = client.c
coap_client@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_LDADD =  $(top_builddir)/.libs/libcoap-$(LIBCOAP_NAME_SUFFIX).la

coap_server@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_SOURCES = coap-server.c
coap_server@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_LDADD = $(top_builddir)/.libs/libcoap-$(LIBCOAP_NAME_SUFFIX).la

coap_rd@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_SOURCES = coap-rd.c
coap_rd@LIBCOAP_DTLS_LIB_EXTENSION_NAME@_LDADD = $(top_builddir)/.libs/libcoap-$(LIBCOAP_NAME_SUFFIX).la

endif # BUILD_EXAMPLES
