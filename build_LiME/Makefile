# Makefile for building LiME

BUILDNAME := lime
HOSTDIR := /Users/jiuweigui/Projects/Environments/build_LiME/out
CONTAINERDIR := /tmp/out

default: build

build:
			docker build -qt $(BUILDNAME) .
			docker run --name=$(BUILDNAME) -d -v $(HOSTDIR):$(CONTAINERDIR) $(BUILDNAME)

rebuild:
			docker run --name=$(BUILDNAME) -d -v $(HOSTDIR):$(CONTAINERDIR) $(BUILDNAME)

clean:
			rm -rf ./out/*.ko

purge:
			docker rm $(shell docker ps -ql)
			docker rmi $(BUILDNAME)
			rm -rf ./out/*.ko
