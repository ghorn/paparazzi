CC = gcc
CFLAGS=-g -O2 -Wall `pkg-config gtk+-2.0 --cflags` -I../../../var/MB
LDFLAGS=`pkg-config gtk+-2.0 --libs` -s -lglibivy

motor_bench : main.c
	$(CC) $(CFLAGS) -g -o $@ $^ $(LDFLAGS)

# -lgtkdatabox

LOG=mb_log.txt

plot_test:
	scilab -f test.sce -args $(LOG)

clean:
	rm -f *~ motor_bench

