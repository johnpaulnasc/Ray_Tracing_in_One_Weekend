# Ray Tracing in One Weekend

## 1. Output an Image

### 1.1 O formato de imagem PPM

Sempre que você inicia um renderizador, precisa de uma maneira de ver uma imagem. A forma mais direta é escrevê-la em um arquivo. A questão é que existem tantos formatos. Muitos deles são complexos. Começo com um arquivo ppm de texto simples. Aqui está uma boa descrição da Wikipedia:

<img style="border-radius:50px;" src="https://raytracing.github.io/images/fig-1.01-ppm.jpg">

Let’s make some C++ code to output such a thing:

\lstset{language=C++}

\begin{lstlisting}
#include <iostream>

int main() {
    std::cout << "Hello, world!" << std::endl;
    return 0;
}
\end{lstlisting}

