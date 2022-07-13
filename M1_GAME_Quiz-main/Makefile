PROJ_NAME = QUIZ_GAME
SRC = main.c functions.c mainhome.c home.c game.c

ifdef OS
   RM = del /q
   FixPath = $(subst /,\,$1)
   EXEC = exe
else
   ifeq ($(shell uname), Linux)
      RM = rm -rf
      FixPath = $1
	  EXEC = out
   endif
endif

all:
	gcc $(SRC) -o $(call FixPath,$(PROJ_NAME).$(EXEC))

run: all
	./$(call FixPath,$(PROJ_NAME).$(EXEC))

clean:
	$(RM) $(call FixPath,$(PROJ_NAME).$(EXEC))
