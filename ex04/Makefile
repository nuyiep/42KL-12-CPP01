# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: plau <plau@student.42.kl>                  +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/04/11 18:01:32 by plau              #+#    #+#              #
#    Updated: 2023/04/13 20:55:15 by plau             ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME			= 	sed
CXX				= 	c++
RM				= 	rm -rf
MKDIR			= 	mkdir -p
CXXFLAGS		= 	-Wall -Wextra -Werror -std=c++98 -pedantic
# CXXFLAGS		+=  -g3 -fsanitize=address
SRCS_FILES		= 	main
SRCS			= 	$(addprefix $(SRCS_DIR), $(addsuffix .cpp, $(SRCS_FILES)))
OBJS			= 	$(addprefix $(OBJS_DIR), $(addsuffix .o, $(SRCS_FILES)))
SRCS_DIR		= 	srcs/
OBJS_DIR		= 	objs/

all:
			  		$(MKDIR) $(OBJS_DIR)
			  		make $(NAME)

$(OBJS_DIR)%.o: 	$(SRCS_DIR)%.cpp
					$(CXX) $(CXXFLAGS) -c $< -o $@

$(NAME):			$(OBJS)
					$(CXX) $(CXXFLAGS) $(OBJS) -o $(NAME)	

clean:
					$(RM) $(OBJS) $(OBJS_DIR)

fclean: 			clean
					$(RM) $(NAME) output.txt

re: 				fclean all

.PHONY:				all clean fclean re