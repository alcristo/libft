*This project has been created as part of the 42 curriculum by [alcristo](https://github.com/alcristo)*

# Libft

## Description

42 projects aim for students to create code using references and peer-to-peer learning. Evaluations are made between students no matter the level between reviewer and evaluated, so the former may help the latter with their experience if their level is higher and the latter may explain the former their code to the former.

This project consists of  creating a C functions library named `libft.a`, which may be extended and used in future projects. Such library aims students to understand how the most elementary functions work. All functions will have the `ft_` prefix.

### Libc functions

All functions in this section have the same purpose as their `libc` counterparts, except for `isalpha`, `isdigit`, `isalnum`, `isascii` and `isprint`, which will return `1` if true. To see each function purpose, refer to the manual.

| Function |
| - |
| `ft_isalpha` |
| `ft_isdigit` |
| `ft_isalnum` |
| `ft_isascii` |
| `ft_isprint` |
| `ft_strlen` |
| `ft_memset` |
| `ft_bzero` |
| `ft_memcpy` |
| `ft_memmove` |
| `ft_strlcpy` |
| `ft_strlcat` |
| `ft_toupper` |
| `ft_tolower` |
| `ft_strchr` |
| `ft_strrchr` |
| `ft_strncmp` |
| `ft_memchr` |
| `ft_memcmp` |
| `ft_strnstr` |
| `ft_atoi` |
| `ft_calloc` |
| `ft_strdup` |

### Additional functions

A set of useful functions. All functions allocate memory except fo the last four involving file descriptors.

| Function | Definition | Description |
| - | - | - |
| `ft_substr` | `char *ft_substr(char const *s, unsigned int start, size_t len)` | Return a substring of `s` from `start` position with length `len` |
| `ft_strjoin` | `char *ft_strjoin(char const *s1, char const *s2)` | Return the resulting string of appending `s2` to `s1` |
| `ft_strtrim` | `char *ft_strtrim(const char *s1, const char *set)` | Return the result of stripping the set of characters `set` at the beginning and at the end of `s1` |
| `ft_split` | `char **ft_split(char const *s, char c)` | Return an array of the strings that compose `s`, separated by `c` |
| `ft_itoa` | `char *ft_itoa(int n)` | Return the string from `n` |
| `ft_strmapi` | `char *ft_strmapi(const char *s, char (*f)(unsigned int, char))` | Return the resulting string of applying function `f` to each character of `s` |
| `ft_striteri` | `void ft_striteri(char *s, void (*f)(unsigned int, char *))` | Apply function `f` to each character of `s` |
| `ft_putchar_fd` | `void ft_putchar_fd(char c, int fd)` | Write character `c` in file descriptor `fd` |
| `ft_putstr_fd` | `void ft_putstr_fd(char *s, int fd)` | Write string `s` in file descriptor `fd` |
| `ft_putendl_fd` | `void ft_putendl_fd(char *s, int fd)` | Write string `s` followed by a newline in file descriptor `fd` |
| `ft_putnbr_fd` | `void ft_putnbr_fd(int n, int fd)` | Write number `n` in file descriptor `fd` |

### Linked lists

Linked lists are data structures composed of nodes connecting another node. Such node is defined by:

```c
typedef struct s_list
{
	void			*content;
	struct s_list	*next;
}
```

| Function | Definition | Description |
| - | - | - |
| `ft_lstnew` | `t_list *ft_lstnew(void *content)` | Allocate memory for a new node with content `content` |
| `ft_lstadd_front` | `void ft_lstadd_front(t_list **lst, t_list *new)` | Add node `new` to the head of `lst` |
| `ft_lstadd_back` | `void ft_lstadd_back(t_list **lst, t_list *new)` | Add node `new` to the tail of `lst` |
| `ft_lstsize` | `int ft_lstsize(t_list *lst)` | Get the size of `lst` |
| `ft_lstlast` | `t_list *ft_lstlast(t_list *lst)` | Get the last node of `lst` |
| `ft_lstdelone` | `void ft_lstdelone(t_list *lst, void (*del)(void *))` | Delete the content of `lst` using `del` and free the node |
| `ft_lstclear` | `void ft_lstclear(t_list **lst, void (*del)(void *))` | Delete the contents of `lst` and the subsequent nodes using `del` and free all nodes |
| `ft_lstiter` | `void ft_lstiter(t_list *lst, void (*f)(void *))` | Apply function `f` to all contents in all nodes of `lst` |
| `ft_lstmap` | `t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))` | Return resulting list of applying function `f` to all contents in all nodes of `lst`. Use `del` if memory allocation fails |

## Instructions

This project has a Makefile with the following rules:

| Rule | Description |
| - | - |
| all | Compile the library |
| clean | Remove temporary objects |
| fclean | Remove temporary objects and library |
| re | Remove temporary objects and library, then compile the library |

To create the library, execute in terminal:

```bash
make all
```

To compile `.c` files using the library, execute:

```bash
[compiler] [-flags] libft.a [files.c]
```

## Resources

Several functions I did during the 42 piscine period were implemented, along with the Piscine Reloaded project.

[Ana Martínez Aguilar's web](https://anamartinezaguilar.medium.com/funciones-para-copiar-vectores-en-c-memcpy-y-memmove-9ce124778801) helped me understand memory management deeper for `memcpy` and `memmove`. No code was implemented until I understood how both functions worked.

[Francinette](https://github.com/xicodomingues/francinette) was used to check the correct functioning of all functions, as well as memory leaks.

### AI usage

AI wasn't used for this project: neither for the functions, nor for code understanding, nor for debugging.
