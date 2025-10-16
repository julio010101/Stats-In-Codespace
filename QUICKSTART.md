# Guia de Início Rápido

## 🎯 Objetivo

Este guia ajudará você a começar rapidamente com o ambiente de estatística usando Jupyter Notebook com R no GitHub Codespaces.

## ⚡ Início Rápido (5 minutos)

### Passo 1: Criar um Codespace

1. Vá para o repositório no GitHub
2. Clique no botão verde **Code**
3. Selecione a aba **Codespaces**
4. Clique em **Create codespace on main**
5. Aguarde a criação (3-5 minutos)

### Passo 2: Verificar a Instalação

Quando o Codespace abrir, aguarde a instalação automática completar. Você verá mensagens no terminal mostrando:
- Instalação do Jupyter
- Instalação do kernel R (IRkernel)
- Instalação de pacotes R (ggplot2, dplyr, etc.)

### Passo 3: Abrir um Notebook

Existem dois notebooks de exemplo incluídos:

1. **exemplo_estatistica.ipynb** - Demonstra análise estatística com R
2. **exemplo_python.ipynb** - Demonstra análise de dados com Python

Para abrir:
1. Clique no notebook no explorador de arquivos
2. No canto superior direito, clique em **Select Kernel**
3. Escolha **R** (para o notebook R) ou **Python 3** (para o notebook Python)

### Passo 4: Executar o Código

1. Clique em uma célula de código
2. Pressione **Shift + Enter** para executar
3. Ou clique no botão ▶️ ao lado da célula

## 📚 Próximos Passos

### Criar Seu Próprio Notebook

1. Clique com o botão direito no explorador de arquivos
2. Selecione **New File**
3. Nomeie o arquivo com extensão `.ipynb` (ex: `meu_notebook.ipynb`)
4. Selecione o kernel desejado (R ou Python)
5. Comece a codificar!

### Instalar Pacotes Adicionais

#### Para R:
```r
install.packages("nome_do_pacote")
```

#### Para Python:
```python
pip install nome_do_pacote
```

### Salvar Seu Trabalho

O Codespace salva automaticamente seus arquivos. Para garantir que suas alterações sejam preservadas:

1. Use Git para commit:
   ```bash
   git add .
   git commit -m "Meu trabalho de estatística"
   git push
   ```

## 🆘 Solução de Problemas

### Kernel R não aparece?

1. Abra um terminal
2. Execute:
   ```bash
   R -e "IRkernel::installspec(user = FALSE)"
   ```
3. Recarregue a janela do VS Code (Ctrl+Shift+P → "Reload Window")

### Pacote não encontrado?

Instale manualmente no terminal:
```bash
# Para R
R -e "install.packages('nome_pacote', repos='https://cloud.r-project.org/')"

# Para Python
pip install nome_pacote
```

### Jupyter não inicia?

1. Abra um terminal
2. Execute:
   ```bash
   pip install --upgrade jupyter jupyterlab
   ```

## 💡 Dicas

1. **Use Shift+Enter** para executar células rapidamente
2. **Ctrl+/** para comentar/descomentar código
3. **Tab** para autocompletar código
4. Use **Markdown** em células de texto para documentação rica
5. Salve frequentemente com **Ctrl+S**

## 📖 Recursos Úteis

- [Documentação R](https://www.r-project.org/other-docs.html)
- [Cheat Sheets R](https://www.rstudio.com/resources/cheatsheets/)
- [Documentação Jupyter](https://jupyter-notebook.readthedocs.io/)
- [Tidyverse](https://www.tidyverse.org/)

## ✅ Checklist de Verificação

Marque quando completar:

- [ ] Codespace criado com sucesso
- [ ] Setup automático completado
- [ ] Kernel R disponível nos notebooks
- [ ] Exemplo de notebook R executado
- [ ] Exemplo de notebook Python executado
- [ ] Primeiro notebook próprio criado

Pronto! Você está preparado para começar suas análises estatísticas! 🎉
