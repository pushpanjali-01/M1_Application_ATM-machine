#Target name : Dependencies
#<TAB>command
# Name of the project
PROJ NAME = ATM-machine
# All source code files
SRC = ATM-machine.c test.h
# All test source files
TEST_SRC = 3_Implementation/.c\
test/test_ATM-machine.c\
unity/unity.c\

TEST_OUTPUT = $(BUILD)/Test_$(PROJ_NAME).out
# Project Output name
PROJECT_OUTPUT = $(BUILD)/$(PROJ_NAME).out

ifdef OS
   RM = del /q
   FixPath = $(sub$t /.\.$1)
   EXEC = exe 
else
   ifeq ($(shell uname), Linux)
      RM = rm -rf
	  FixPath = $1
	  EXEC = out
	endif
endif
# Call `make run` to run the application
$(PROJ_NAME) : $(SRC)
     gcc $(SRC) -o $(call Fixpath, $(PROJ_NAME).$(EXEC))
run : $(PROJ_NAME)
    ./$(call FixPath, $(PROJ_NAME).$(EXEC))

# Remove all the built files, invoke by `make clean`
clean:
     rm -rf *.out
