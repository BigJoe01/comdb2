COMDB2_UNITTEST=1
ifeq ($(TESTSROOTDIR),)
  include ../testcase.mk
else
  include $(TESTSROOTDIR)/testcase.mk
endif

glgetopt: getopt_test.c $(SRCHOME)/bb/bb_getopt_long.c $(SRCHOME)/bb/bb_getopt_long.h
	gcc -g -DNORMAL_GETOPT -std=c99 $(CURRDIR)/getopt_test.c $(SRCHOME)/bb/bb_getopt_long.c -I$(SRCHOME)/bb -o glgetopt

bbgetopt: getopt_test.c $(SRCHOME)/bb/bb_getopt_long.c $(SRCHOME)/bb/bb_getopt_long.h
	gcc -g -std=c99 $(CURRDIR)/getopt_test.c $(SRCHOME)/bb/bb_getopt_long.c -I$(SRCHOME)/bb -o bbgetopt

unit: glgetopt bbgetopt
	
clean::
	rm -f glgetopt bbgetopt *bb *gl
