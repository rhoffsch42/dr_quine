# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rhoffsch <rhoffsch@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2015/05/15 17:38:19 by rhoffsch          #+#    #+#              #
#    Updated: 2017/07/03 16:41:53 by rhoffsch         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME			=	Colleen
CC				=	gcc
CFLAGS			=	-Wall -Wextra -Werror

SRC				=	Colleen.c

OBJ_DIR			=	obj
OBJ				=	$(patsubst %.c, $(OBJ_DIR)/%.o, $(SRC))

.PHONY: all compile clean fclean re

all: compile

compile:
	@mkdir -p $(OBJ_DIR)
	@$(MAKE) $(NAME)

$(NAME): $(SRC) $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)

$(OBJ_DIR)/%.o: $(SRC)
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf $(OBJ_DIR)

fclean: clean
	rm -f $(NAME)

re: fclean all
