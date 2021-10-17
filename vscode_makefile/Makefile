APP_NAME = application

CC = g++
CFLAGS = -g -c -Wall

SRC_DIR = src/
SRC_FILES = $(wildcard $(SRC_DIR)*)
FILES_NAMES = $(basename $(notdir $(SRC_FILES)))

INC_DIR = inc/

OBJ_DIR = obj/
OBJ_FILES = $(addprefix $(OBJ_DIR), $(addsuffix .o, $(FILES_NAMES)))

$(APP_NAME): $(OBJ_FILES)
	$(CC) -I$(INC_DIR) -o $@ $^

define build-obj
	$(CC) -I$(INC_DIR) $(CFLAGS) $^ -o $@
endef

$(OBJ_DIR)%.o: $(SRC_DIR)%.cpp
	$(call build-obj)

clean:
	rm	-rf *.s $(OBJ_DIR)*.o *.exe Logfile.txt