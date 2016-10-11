InDir = ../Styles
Files = $(shell cd '$(InDir)' && find . -type f -name '*.scss' )
OutFiles := $(Files:%.scss=%.css)

all : $(OutFiles)

%.css : $(InDir)/%.scss
	scss --sourcemap=none --style expanded $< $@

clean :
	-rm $(OutFiles)
