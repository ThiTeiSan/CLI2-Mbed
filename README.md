# CLI2-Mbed

## 1. Instalando dependências

### 1.0. Caso não tenha, instale python
O python do anaconda pode apresentar problemas. Caso não tenha o python fora o do anaconda (ou não tenha certeza), baixe a última versão do python: https://www.python.org/downloads/

### 1.1. Dependências com pip install:
1. Abra a prompt de comando (cmd no Menu Iniciar Windows)
2. Digite e rode os seguintes comandos (para instalar o ninja e o Jinja2):
- pip install -U Jinja2
- python -m pip install ninja
  
![image](https://github.com/ThiTeiSan/CLI2-Mbed/assets/167451264/234b9324-3ea4-4eec-bb60-dca419b8885e)

### 1.2. Instalando CMAKE:
Vá no link: https://cmake.org/download/

Abaixo de "Binary distributions", clique na última versão que deseja instalar. Para windows, clique no que contenha "Windows x64 Installer"

![image](https://github.com/ThiTeiSan/CLI2-Mbed/assets/167451264/d46311f8-e886-427b-b23e-11d0815b92c5)

### 1.3. Instalando o toolchain da arm:
Acesse o link: https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads

Baixe o .exe do "arm-gnu-toolchain-13.2.rel1-mingw-w64-i686-arm-none-eabi"

![image](https://github.com/ThiTeiSan/CLI2-Mbed/assets/167451264/005714d3-b23d-40ea-a9bf-2d97d0cd3228)






## 2. Instalando o CLI 2 do Mbed

1. Abra a prompt de comando (repita os passos de 1.1) e digite e rode o código:
- python -m pip install mbed-tools
2. Para saber se funcionou, rode o comando:
- mbed-tools --help

Resultado esperado:

![image](https://github.com/ThiTeiSan/CLI2-Mbed/assets/167451264/d34c4986-bf77-4f00-a0b6-6e802a3a7cbe)


## 3. Utilizando o CLI 2
Agora que tudo está intalado, aqui segue alguns comandos úteis para a utilização do CLI 2

### 3.1. Detectando uma placa
Conecte alguma placa no computador e rode o comando:
- mbed-tools detect

Resultado esperado (para placa Nucleo F303RE):

![image](https://github.com/ThiTeiSan/CLI2-Mbed/assets/167451264/f754a589-7b29-4d21-9cb3-43a089ac2ef4)

### 3.2. Criando um novo projeto

O comando
- mbed-tools new \<PATH>

Cria um novo projeto, importando uma versão do Mbed OS 6. "\<PATH>" é o diretório onde o projeto será configurado. Por exemplo "mbed-tools new .\aps_4" cria uma pasta "aps_4" e baixa os arquivos para dentro dela.

> [!WARNING]
> O comando "mbed-tools new \<PATH>" baixa uma nova versão do Mbed OS toda vez que ele é rodado (+- 1GB). Você pode rodar "mbed-tools new -c <PATH>" onde o "-c" previne o download de uma nova versão, e você pode copiar de um outro projeto.

Adicionalmente, é possível importar projetos de exemplo da Mbed através do comando
- mbed-tools import \<example> \<PATH>

Por exemplo, o comando "mbed-tools import mbed-os-example-blinky \<PATH>" irá baixar o exemplo blinky.



### 3.3 Compilando um projeto

