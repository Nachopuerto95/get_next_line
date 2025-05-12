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

## 📜 Sobre el Proyecto

> Cada vez que llamamos a esta función, recibiremos la siguiente línea del descriptor de archivo dado. \

```html
         🚀 Aprenderás cómo se abren, leen y cierran los archivos en un sistema operativo,
         y cómo son interpretados por un lenguaje de programación. Aprenderemos
         sobre descriptores de archivo, manejo de buffers y memoria dinámica.
```

> [!NOTE]
> Debido a los requisitos de la norma de la Escuela 42:
> * Cada función no puede tener más de 25 líneas de código.
> * Todas las variables deben ser declaradas y alineadas al inicio de cada función.
> * El proyecto debe realizarse únicamente con funciones permitidas.
<br>

### 🛠️ Uso

#### Instrucciones

1. Usarlo en tu código

Para usar la función en tu código, simplemente incluye su cabecera:

```c
#include "get_next_line.h"
```

Y, al compilar tu código, añade los archivos fuente y la bandera requerida:

```shell
get_next_line.c get_next_line_utils.c -D BUFFER_SIZE=<tamaño>
```

Luego, solo necesitas llamar a la función pasando un `fd`. Ejemplo:

```c
int	fd;
char	*line;

fd = open(file, O_RDONLY);
line = get_next_line(fd);
```

#### Parte Bonus

Para usar la "parte bonus", solo necesitas abrir dos descriptores de archivo, luego puedes alternar entre llamadas y obtendrás una mezcla de ambos.
Mira este ejemplo alternando las primeras 3 líneas de *Harry Potter* y *El Quijote*:

```c
int	fd1;
int	fd2;

fd1 = open("Quixote", O_RDONLY);
fd2 = open("HarryPotter", O_RDONLY);
printf("%s", get_next_line(fd1));
printf("%s", get_next_line(fd2));
printf("%s", get_next_line(fd1));
printf("%s", get_next_line(fd2));
printf("%s", get_next_line(fd1));
printf("%s", get_next_line(fd2));
```

#### Salida esperada:

```html
$ > En un lugar de la Mancha, de cuyo nombre no quiero acordarme...
$ > El señor y la señora Dursley, que vivían en el número cuatro de Privet Drive, estaban orgullosos de decir que eran muy normales, afortunadamente.
$ > No ha mucho tiempo que vivía un hidalgo de los de lanza en astillero, adarga antigua, rocín flaco y galgo corredor.
$ > Eran las últimas personas que se esperaría ver relacionadas con algo extraño o misterioso, porque no estaban para tales tonterías.
$ > Una olla de algo más vaca que carnero, salpicón las más noches, duelos y quebrantos los sábados...
$ > El señor Dursley era director de una empresa llamada Grunnings, que fabricaba taladros.
$ >
```
