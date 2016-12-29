InDir = ../Styles
Files = $(shell cd '$(InDir)' && find . -type f -name '[^_]*.scss' )
Deps = $(shell find '$(InDir)' -type f -name '_*.scss' )
OutFiles := $(Files:%.scss=%.css)

all : $(OutFiles)

%.css : $(InDir)/%.scss $(Deps)
	scss --sourcemap=none --style expanded $< $@ || { Res=$$? ; rm $@ ; ( exit $$Res ) }

clean :
	-rm $(OutFiles)
