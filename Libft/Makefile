# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rkhakimu <rkhakimu@student.hive.fi>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/04/30 12:45:23 by rkhakimu          #+#    #+#              #
#    Updated: 2024/10/27 08:51:42 by rkhakimu         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# Project settings
NAME        = libft.a
CC          = cc
CFLAGS      = -Wall -Wextra -Werror

# Source files
SRC         = ft_isascii.c ft_memcpy.c ft_strlcat.c ft_strrchr.c ft_bzero.c \
              ft_isdigit.c ft_memmove.c ft_strlcpy.c ft_tolower.c ft_calloc.c \
              ft_isprint.c ft_memset.c ft_strlen.c ft_toupper.c ft_isalnum.c \
              ft_memchr.c ft_strchr.c ft_strncmp.c ft_isalpha.c ft_memcmp.c \
              ft_strdup.c ft_strnstr.c ft_atoi.c ft_strdup.c ft_substr.c \
              ft_strjoin.c ft_strtrim.c ft_split.c ft_itoa.c ft_strmapi.c \
              ft_striteri.c ft_putchar_fd.c ft_putstr_fd.c ft_putendl_fd.c \
              ft_putnbr_fd.c ft_printchar.c ft_printf.c ft_printhex.c \
              ft_printhex_ptr.c ft_printnbr.c ft_printstr.c ft_printunbr.c \
              get_next_line.c get_next_line_utils.c

SRC_BONUS   = ft_lstnew_bonus.c ft_lstadd_front_bonus.c ft_lstsize_bonus.c \
              ft_lstlast_bonus.c ft_lstadd_back_bonus.c ft_lstdelone_bonus.c \
              ft_lstclear_bonus.c ft_lstiter_bonus.c ft_lstmap_bonus.c

# Object files
OBJ         = $(SRC:.c=.o)
OBJ_BONUS   = $(SRC_BONUS:.c=.o)

.PHONY: all clean fclean re bonus

# Default target to build the library
all: $(NAME)

# Rule to create the static library
$(NAME): $(OBJ)
	@ar -rcs $(NAME) $(OBJ)
	@echo "Libft library created: $(NAME)"

# Rule for bonus files
bonus: $(OBJ) $(OBJ_BONUS)
	@ar -rcs $(NAME) $(OBJ) $(OBJ_BONUS)
	@echo "Libft bonus features added to: $(NAME)"

# Compilation rule for object files
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Clean object files
clean:
	rm -f $(OBJ) $(OBJ_BONUS)
	@echo "Object files removed."

# Full clean, including the static library
fclean: clean
	rm -f $(NAME)
	@echo "Library and object files removed."

# Rebuild the entire library from scratch
re: fclean all
