KERN_DIR = /home/bear/workspace/s3c-linux.jyx

INSTALL_DIR = ./bin
EXP_INSTALL = install -m 755 
EXEC =  ./register_major.ko

all:
	make -C $(KERN_DIR) M=`pwd` modules 
	$(EXP_INSTALL) $(EXEC) $(INSTALL_DIR)
	$(EXP_INSTALL) $(EXEC) /nfsroot
clean:
	make -C $(KERN_DIR) M=`pwd` modules clean
	rm -rf modules.order *~

obj-m	+= register_major.o
