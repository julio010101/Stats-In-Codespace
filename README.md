# Stats-In-Codespace
Ambiente de laboratório para aulas de estatística e ciência de dados via Jupyter Notebook

## 📊 Sobre

Este repositório fornece um ambiente de desenvolvimento para estatística e ciência de dados usando **Jupyter Notebook** com suporte ao **R**, ao **Python** e SGBD **ClickHouse** no **VS Code** através do **GitHub Codespaces**.

## 🚀 Como Usar

### Opção 1: GitHub Codespaces (Recomendado)

1. Clique no botão **Code** (verde) no topo deste repositório
2. Selecione a aba **Codespaces**
3. Clique em **Create codespace on main** (ou no branch desejado)
4. Aguarde a criação do ambiente (pode levar alguns minutos na primeira vez)
5. O ambiente será configurado automaticamente com:
   - Python e Jupyter Notebook
   - R e IRkernel (kernel R para Jupyter)
   - Pacotes R comuns para estatística (ggplot2, dplyr, tidyr, etc.)
   - Extensões do VS Code para Jupyter e R

### Opção 2: Desenvolvimento Local

Se preferir trabalhar localmente, você precisará ter o Docker instalado:

1. Clone este repositório:
   ```bash
   git clone https://github.com/FGV-Fundacao-Getulio-Vargas/Stats-In-Codespace.git
   cd Stats-In-Codespace
   ```

2. Abra no VS Code:
   ```bash
   code .
   ```

3. O VS Code detectará o arquivo `.devcontainer` e perguntará se deseja reabrir no container
4. Clique em **Reopen in Container**

## 📝 Usando Jupyter Notebooks

### No VS Code

1. Abra ou crie um arquivo `.ipynb`
2. Clique em **Select Kernel** no canto superior direito
3. Escolha o kernel conectando-se ao ambiente codespace (se estiver no codespace)
4. Abra os exemplos indicados pelo professor, compreenda e atualize conforme a sua evolução

### Via Terminal

Você também pode iniciar o Jupyter Notebook ou JupyterLab via terminal:

```bash
# Jupyter Notebook
jupyter notebook

# JupyterLab (interface moderna)
jupyter lab
```

## 📚 Exemplo

Um notebook de exemplo está incluído: `exemplo_estatistica.ipynb`

Este exemplo demonstra:
- Carregamento de bibliotecas R
- Criação de dados
- Estatísticas descritivas
- Visualização de dados com ggplot2
- Análise por grupos com dplyr

## 🔧 Pacotes R Instalados

Os seguintes pacotes R estão pré-instalados:

- **IRkernel**: Kernel R para Jupyter
- **ggplot2**: Visualização de dados
- **dplyr**: Manipulação de dados
- **tidyr**: Organização de dados
- **readr**: Leitura de dados
- **tibble**: Data frames modernos
- **stringr**: Manipulação de strings
- **forcats**: Trabalho com fatores
- **purrr**: Programação funcional

## 📦 Instalando Pacotes Adicionais

Para instalar pacotes R adicionais, use o terminal:

```r
R -e "install.packages('nome_do_pacote', repos='https://cloud.r-project.org/')"
```

Ou dentro de um notebook:

```r
install.packages("nome_do_pacote")
```

## 🛠️ Extensões VS Code Incluídas

- **Jupyter**: Suporte completo para notebooks Jupyter
- **Python**: Suporte para Python
- **R**: Suporte para linguagem R
- **R LSP**: Language Server Protocol para R (autocompletar, linting)

## 📖 Recursos Adicionais

- [Documentação Jupyter](https://jupyter.org/documentation)
- [Documentação R](https://www.r-project.org/)
- [IRkernel](https://irkernel.github.io/)
- [GitHub Codespaces](https://github.com/features/codespaces)

## Referências

- Fávero, L. P.; Belfiore, P. Manual de Análise de Dados. 1ª Edição. Rio de Janeiro: Elsevier, 2017.
- Book, Velleman, De Veaux; Stats: Modeling the World. Pearson, 2016.
- Statistics: the art and science of learning from data; Agresti, Franklin, Klingenberg; 2007.
- The Art of Statistics: How to Learn from Data; David Spiegelhalter.
- Inteligência Computacional: Fundamentos e Aplicações; Alexandre Evsukoff; 2020.

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## 📄 Licença

Este projeto é de código aberto e está disponível para uso educacional.
