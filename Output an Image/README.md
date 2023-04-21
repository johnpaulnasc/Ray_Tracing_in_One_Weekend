# Ray Tracing in One Weekend

## 1. Produzir/gerar uma imagem

### 1.1 O formato de imagem PPM

Sempre que você inicia um renderizador, precisa de uma maneira de ver uma imagem. A forma mais direta é escrevê-la em um arquivo. A questão é que existem tantos formatos. Muitos deles são complexos. Começo com um arquivo ppm de texto simples. Aqui está uma boa descrição da Wikipedia:

<img style="border-radius:50px;" src="https://raytracing.github.io/images/fig-1.01-ppm.jpg">

Vamos criar um código em C++ para produzir algo assim:

```cpp
#include <iostream>

int main() {

    // Image

    const int image_width = 256;
    const int image_height = 256;

    // Render

    std::cout << "P3\n" << image_width << ' ' << image_height << "\n255\n";

    for (int j = image_height-1; j >= 0; --j) {
        for (int i = 0; i < image_width; ++i) {
            auto r = double(i) / (image_width - 1);
            auto g = double(j) / (image_height - 1);
            auto b = 0.25;

            int ir = static_cast<int>(255.999 * r);
            int ig = static_cast<int>(255.999 * g);
            int ib = static_cast<int>(255.999 * b);

            std::cout << ir << ' ' << ig << ' ' << ib << '\n';
        }
    }
}
```
 [Creating your first image](https://github.com/jonhpaul5/Ray_Tracing_in_One_Weekend/blob/master/Output%20an%20Image/ppmExemple.cpp)

