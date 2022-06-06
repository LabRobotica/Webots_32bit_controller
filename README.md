# Webots LibController 32bit

Compilação de 32bit das bibliotecas compartilhadas [controller](https://github.com/cyberbotics/webots/tree/master/src/controller) do [Webots](https://cyberbotics.com/).

## Instalação

Para instalar as bibliotecas no sistema apenas execute os comandos:

```bash
sudo mv libController.so /usr/lib32/
```

e

```bash
sudo mv libCppController.so /usr/lib32/
```

## Versão

A versão disponibilizada é compilada a partir da versão 2022a. Talvez seja possível utilizar em outras versões.

## Uso

Apenas coloque a flag de compilação, e de linkamento, de 32 bits no makefile do seu controlador C/C++.

```Makefile
CFLAGS = -m32
LFLAGS = -m32
```

## Motivação

Porque compilar um controlador de 32bits?
Porque algumas bibliotecas compartilhadas que eventuamente precisem ser linkadas ao projeto podem estar disponíveis apenas para 32bits. Com essa biblioteca de 32bits agora é possível compilar um controlador 32bits para o Webots linkando bibliotecas exclusivamente compiladas para 32bits, como é o caso de algumas bibliotecas linkadas a alguns projetos do Webots do laboratório.
