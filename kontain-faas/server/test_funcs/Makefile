KONTAINGCC = /opt/kontain/bin/kontain-gcc
KONTAININCL = /opt/kontain/include

all:	test_func1 test_func_data_with_hc.km

test_func1: test_func1.c

test_func_data_with_hc.km:	test_func_data_with_hc.c
	${KONTAINGCC} -o test_func_data_with_hc.km -I${KONTAININCL} test_func_data_with_hc.c

test_func_km: test_func_km.c

clean:
	rm -f test_func1 test_func_km test_func_data_with_hc.km

images: test_func_km
	docker build -t test_func_1 -f test_func_1.dockerfile  .
	docker build -t test_func_2 -f test_func_2.dockerfile  .
