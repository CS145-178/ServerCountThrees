# Name: Nevin Greene
# Course: CS178 Build Automation for DevOps and QA
# CRN: 76718
# Date: 02/18/20
# Assignment: ServerCountThrees Makefile c

# runner for the executable, first so default
runServerCountThrees : ServerCountThrees
	./ServerCountThrees

# build the executable
ServerCountThrees : ServerCountThrees.c readInt32BitLE.c readInt32BitLE.h 
	gcc ServerCountThrees.c readInt32BitLE.c -o ServerCountThrees

# remove the executable
clean : ServerCountThrees
	rm ServerCountThrees


# test target per reqs - only removes the build dir if exists
test : 
	rm -rf ../build
	mkdir ../build
	cp ServerCountThrees ../build/ServerCountThrees
	cp ../data/threesData.bin ../build/threesData.bin
	./../build/ServerCountThrees