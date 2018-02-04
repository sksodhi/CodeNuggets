#
# Makefile
#
# Created by Sandesh Kumar Sodhi, January 2018
# Copyright (c) 2018 Sandesh Kumar Sodhi
#
# Notice and Disclaimer: This code is licensed to you under the MIT license.
#

CXX = g++
PROG = readjsoncfg

CXXFLAGS += -g -O0 -std=c++11

CPPFLAGS += \
	-I. \
	-I/usr/include/jsoncpp

LDLIBS = \
		 -ljsoncpp

LDFLAGS += -L/usr/local/lib $(LDLIBS)

all: $(PROG)
	@echo $(PROG) compilation success!

SRCS = \
	ReadJsonCfg.cpp
OBJS=$(subst .cc,.o, $(subst .cpp,.o, $(SRCS)))

$(PROG): $(OBJS)
	$(CXX) $^ $(LDFLAGS) -o $@

clean:
	rm -f $(OBJS) $(PROG) ./.depend

depend: .depend

.depend: $(SRCS)
	rm -f ./.depend
	$(CXX) $(CXXFLAGS) $(CPPFLAGS) -MM $^ >  ./.depend;

include .depend
