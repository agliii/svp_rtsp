
#CROSS_COMPILE=arm-hisiv300-linux-
#CROSS_COMPILE=arm-linux-uclibceabi-
CROSS_COMPILE=aarch64-mix210-linux-
CC=$(CROSS_COMPILE)gcc
CXX=$(CROSS_COMPILE)g++
AR=$(CROSS_COMPILE)ar
RANLIB= $(CROSS_COMPILE)ranlib
STRIP=$(CROSS_COMPILE)strip

TARGET = librtsp.a

#CC ?= arm-hisiv300-linux-gcc
CC ?= aarch64-mix210-linux 
CFLAGS += -g -Wall -D__LINUX__
#CFLAGS += -g -Wall 

all : rtsp_demo.o rtsp_msg.o rtp_enc.o stream_queue.o utils.o

	$(AR) -r $(TARGET) *.o
	###cp $(TARGET) ../

%.o: %.c
    ##$(CC) -c $(CFLAGS) -o $@ $<
	$(CC) -c $(CFLAGS) -o $@ $^

clean :
	/bin/rm -f *.o
	/bin/rm -f $(TARGET)
