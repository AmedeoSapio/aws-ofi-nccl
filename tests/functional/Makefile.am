#
# Copyright (c) 2018-2023, Amazon.com, Inc. or its affiliates. All rights reserved.
#
# See LICENSE.txt for license information
#


AM_CPPFLAGS = -I$(top_srcdir)/include $(MPI_CPPFLAGS) $(CUDA_CPPFLAGS)
AM_LDFLAGS = $(MPI_LDFLAGS) $(CUDA_LDFLAGS)
LDADD = $(top_builddir)/src/libinternal_net_plugin.la $(MPI_LIBS) $(CUDA_LIBS)
CC = $(MPICC)

noinst_HEADERS = test-common.h

if ENABLE_TESTS
bin_PROGRAMS = nccl_connection nccl_message_transfer ring
endif

nccl_connection_SOURCES = nccl_connection.c
nccl_message_transfer_SOURCES = nccl_message_transfer.c
ring_SOURCES = ring.c
