
VIEWBASE   := $(shell echo `pwd` | sed -e 's/\/STCM_Application\/.*//')

.PHONY: all

all:
	@echo "*************************"
	@echo "A52 decoder build start  "
	@echo "*************************"
	cd a52dec-0.7.4; make
	cd ..	
	@echo "*************************"
	@echo "A52 decoder build end    "
	@echo "*************************"
	@echo "*************************"
	@echo "MPEG2 decoder build start"
	@echo "*************************"
	cd libmpeg2-0.5.1; make 
	cd ..	
	@echo "*************************"
	@echo "MPEG2 decoder build end  "
	@echo "*************************"

clean: depend localclean

depend:
	@echo "*************************"
	@echo "A52 decoder configure    "
	@echo "*************************"
	cd a52dec-0.7.4;./configure
	cd ..
	@echo "*************************"
	@echo "MPEG2 decoder configure  "
	@echo "*************************"
	cd libmpeg2-0.5.1;./configure
	cd ..

localclean:
	@echo "*************************"
	@echo "A52 decoder clean        "
	@echo "*************************"
	cd a52dec-0.7.4;make clean
	cd ..
	@echo "*************************"
	@echo "MPEG2 decoder clean      "
	@echo "*************************"
	cd libmpeg2-0.5.1;make clean
	cd ..

