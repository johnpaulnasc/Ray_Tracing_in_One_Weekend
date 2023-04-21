# Ray Tracing in One Weekend

## 1. Output an Image

### 1.1 O formato de imagem PPM

Sempre que você inicia um renderizador, precisa de uma maneira de ver uma imagem. A forma mais direta é escrevê-la em um arquivo. A questão é que existem tantos formatos. Muitos deles são complexos. Começo com um arquivo ppm de texto simples. Aqui está uma boa descrição da Wikipedia:

<img style="border-radius:50px;" src="https://raytracing.github.io/images/fig-1.01-ppm.jpg">

Let’s make some C++ code to output such a thing:

- [[main.cc] Creating your first image](https://github.com/jonhpaul5/Ray_Tracing_in_One_Weekend/blob/master/Output%20an%20Image/ppmExemple.cpp)

