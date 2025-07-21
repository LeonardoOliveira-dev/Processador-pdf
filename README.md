# Processador-pdf

Ferramenta Python para automação e limpeza de dados em PDF.

Esse é um projeto pessoal desenvolvido em Python com o objetivo de automatizar o processamento de arquivos PDF. Criei a ferramenta pensando em situações do dia a dia onde há necessidade de separar e organizar documentos em lote com base em uma planilha de referência.

## Funcionalidades

- Leitura automatizada de arquivos PDF em uma pasta
- Verificação de nomes com base em uma planilha Excel
- Separação de arquivos por número identificador
- Cópia dos arquivos válidos para uma pasta final
- Interface simples via janelas pop-up (Tkinter)

## Tecnologias utilizadas

- Python 3
- pandas
- openpyxl (para ler Excel)
- shutil, os, glob (nativas)
- tkinter (interface gráfica nativa)

## Como usar

1. (https://github.com/LeonardoOliveira-dev/Processador-pdf/blob/main/.gitignore)
2. Instale as dependências:
3. Prepare os arquivos:
- Coloque o Excel `Arquivos a separar.xlsx` na raiz do projeto
- Coloque os PDFs dentro da pasta `Pdf/`
4. Execute o script:
Os arquivos válidos serão copiados para a pasta `Selecionados/`.

## Estrutura esperada

Processador-pdf/
├── main.py
├── Arquivos a separar.xlsx
├── Pdf/
│ └── seus_arquivos.pdf
├── Selecionados/






