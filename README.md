# [Nome do seu Projeto - Ex: Portfólio de NLP e Machine Learning]

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.25.0-red?style=for-the-badge&logo=streamlit)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab)
![Scikit-learn](https://img.shields.io/badge/SciKit_Learn-F7931E?style=for-the-badge&logo=scikitlearn)

Este repositório contém uma coleção de projetos focados em **Processamento de Linguagem Natural (NLP)** e **Machine Learning**, com visualizações de dados interativas construídas usando **Streamlit**.

O diferencial deste repositório é que todos os projetos foram desenvolvidos e configurados para serem executados diretamente no ambiente do **Google Colab**.

---

## 🚀 Projetos Incluídos

Aqui você pode listar os projetos. Seja descritivo.

* **Projeto 1: Análise de Sentimentos de Tweets**
    * **Descrição:** Um modelo de NLP que classifica tweets como positivos, negativos ou neutros.
    * **Tecnologias:** NLTK, Scikit-learn, Regressão Logística.
    * **Visualização:** Dashboard no Streamlit mostrando a distribuição dos sentimentos e permitindo teste com novas frases.
    * **Notebook:** `[Link_para_seu_notebook_1.ipynb]`

* **Projeto 2: Sistema de Recomendação de Filmes**
    * **Descrição:** Um sistema de recomendação baseado em conteúdo (content-based filtering).
    * **Tecnologias:** Pandas, Scikit-learn (TfidfVectorizer, cosine_similarity).
    * **Visualização:** Interface no Streamlit onde você digita o nome de um filme e recebe 10 recomendações.
    * **Notebook:** `[Link_para_seu_notebook_2.ipynb]`

* **Projeto 3: [Seu Próximo Projeto]**
    * **Descrição:** [Descreva o que ele faz]
    * **Tecnologias:** [Tecnologias usadas]
    * **Visualização:** [Descreva o dashboard]
    * **Notebook:** `[Link_para_seu_notebook_3.ipynb]`

---

## 🛠️ Como Executar (Instruções Cruciais)

Estes projetos **não** devem ser executados localmente da forma tradicional (`streamlit run app.py`) sem adaptação. Eles foram criados para rodar no Google Colab.

### Método 1: Abrir no Google Colab (Recomendado)

A forma mais fácil de executar qualquer projeto é usando o botão "Open in Colab" (se você configurar) ou abrindo os arquivos `.ipynb` diretamente no Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/[SEU-USUARIO-GITHUB]/[SEU-REPOSITORIO]/blob/main/[CAMINHO-PARA-O-NOTEBOOK.ipynb])

*(**Instrução para você:** Substitua o link acima pelo link direto do seu notebook no GitHub. Faça um para cada projeto.)*

### Método 2: Execução Manual no Colab

Se você abrir o notebook manualmente:

1.  Abra o arquivo `.ipynb` no [Google Colab](https://colab.research.google.com/).
2.  Execute as células de instalação de bibliotecas (geralmente no topo do notebook). Elas devem incluir `streamlit` e `pyngrok`:
    ```python
    !pip install streamlit pyngrok -q
    ```
3.  Execute todas as células do projeto.
4.  A **última célula** do notebook será responsável por iniciar o Streamlit e criar um túnel público (usando `pyngrok`) para você acessar a visualização. Ela deve parecer com isto:

    ```python
    # Salva o código do app Streamlit em um arquivo .py
    %%writefile app.py
    import streamlit as st
    # ... (todo o seu código do Streamlit aqui) ...
    # Ex: st.title('Meu App de NLP')
    # ... (resto do seu código) ...

    # Inicia o Streamlit em background e cria o túnel com pyngrok
    !streamlit run app.py &>/dev/null&
    from pyngrok import ngrok
    public_url = ngrok.connect(port='8501')
    print(f'Clique aqui para acessar o app: {public_url}')
    ```
5.  Clique no link (URL) gerado pela saída da última célula para ver seu dashboard Streamlit rodando.

---

## 💻 Execução Local (Alternativa Avançada)

Se você **realmente** quiser rodar estes projetos localmente, você precisará adaptar os notebooks:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/](https://github.com/)[SEU-USUARIO-GITHUB]/[SEU-REPOSITORIO].git
    cd [SEU-REPOSITORIO]
    ```
2.  **Crie um ambiente virtual:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: venv\Scripts\activate
    ```
3.  **Instale as dependências:**
    (Você deve criar um arquivo `requirements.txt` com todas as bibliotecas usadas)
    ```bash
    pip install -r requirements.txt
    ```
4.  **Adapte o Código:** Você precisará extrair o código do Streamlit (o que está dentro do `%%writefile app.py`) para um arquivo Python separado (ex: `app_local.py`).
5.  **Execute localmente:**
    ```bash
    streamlit run app_local.py
    ```

---

## 👨‍💻 Autor

* **[Igor Barbosa]**
* **LinkedIn:** [(https://www.linkedin.com/in/igor-barbosa-negreiros)]
