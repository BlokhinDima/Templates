# Simple makefile template
#
# Create the following structure in makefile root folder
#
##########################
# STRUCTURE OF PROJECT:
# (you)-|
#       |--->obj
#       |
#       |--->src
#       |
#       |--->inc
##########################

CC = g++

APP = program

CFLAGS = -g3 -c -Wall

SRC_DIR = src/
SRC_FILES = $(basename $(notdir $(wildcard $(SRC_DIR)*)))

INC_DIR = inc/

OBJ_DIR = obj/
OBJ_FILES := $(addprefix $(OBJ_DIR), $(addsuffix .o, $(SRC_FILES)))

$(APP): $(OBJ_FILES)
	$(CC) -o $@ $^

define build-obj
	$(CC) $(CFLAGS) -I$(INC_DIR) $^ -o $@
endef

$(OBJ_DIR)%.o: $(SRC_DIR)%.cpp
	$(call build-obj)

.PHONY: clean
clean:
	rm -rf $(APP) $(OBJ_DIR)*.o
