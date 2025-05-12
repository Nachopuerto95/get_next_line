<p align="end">
   <strong>🌐 Change language:</strong><br>
   <a href="README.es.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/ES.png" alt="Español" width="50">
  </a>&nbsp;&nbsp;&nbsp;
  <a href="/README.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/EN.png" alt="English" width="50">
  </a>
</p>

<h1>🧵 Get_next_line (42 cursus)</h1>

<img src="https://github.com/Nachopuerto95/multilang/blob/main/42-Madrid%20-%20Edited.jpg">

## 📜 About Project

> Every time we call this function, we will recive the next line of the file descriptor given \

	🚀 You will understand how files are opened, read and closed in an OS,
    and how they are interpreted by a programming language, we will learn
    about file descriptor, handling buffers and dynamic memory.

> [!NOTE]  
> Because of 42 School norm requirements:
> * Each function can't have more than 25 lines of code.
> * All variables are declared and aligned at the top of each function.
> * Project should be created just with allowed functions.
<br>

### 🛠️ Usage

Instructions
1. Using it in your code

To use the function in your code, simply include its header:

```c
#include "get_next_line.h"
````
and, when compiling your code, add the source files and the required flag:

```shell
get_next_line.c get_next_line_utils.c -D BUFFER_SIZE=<size>
```
Then you just need to call the function passing a fd, Example:

```c
int	fd;
char	*line;

fd = open(file, O_RDONLY);
line = get_next_line(0);
```
