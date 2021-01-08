# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rbourgea <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/09/11 16:36:54 by rbourgea          #+#    #+#              #
#    Updated: 2019/09/15 13:18:39 by rbourgea         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a

PATH = ./srcs/

SRCS = ${PATH}ft_putchar.c ${PATH}ft_swap.c ${PATH}ft_putstr.c ${PATH}ft_strlen.c ${PATH}ft_strcmp.c

OBJS= ${SRCS:.c=.o}

H_DIR = ./includes/

H_SRCS = ${H_DIR}ft.h

FLAGS = -Wall -Wextra -Werror

OPTIONS = -c ${SRCS} -I${H_DIR}

all: ${NAME}

.c.o:
	gcc -Wall -Wextra -Werror -c $< -o $(<:.c=.o) -I${H_DIR}

${NAME}: ${OBJS}
	ar rc ${NAME} ${OBJS}

clean:
	/bin/rm -f ${OBJS}

fclean: clean
	/bin/rm -f ${NAME}

re: fclean all
	.PHONY: re fclean clean all .c.o
