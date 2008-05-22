#
# libLensFun makefile
# Requirements: GNU Make >=3.80
#

-include config.mak
# Local user file which can be used to override some of the settings (e.g. MODE)
-include local-config.mak

ifndef TARGET
$(error You must run configure before starting compiling)
endif

# Default include directories
DIR.INCLUDE.CXX = include

# Default build mode
MODE ?= release

# We want to always build dependencies (no need for "make dep")
# (only if the 'out/blah/' directory has been created, though)
AUTODEP ?= $(if $(wildcard $(OUT)),1)

# Build tools if they aren't available
ifndef MAKEDEP
MAKEDEP = $(OUT)makedep$(EXE)
MAKEDEP_DEP = $(MAKEDEP)
endif

include build/mak/rules.mak