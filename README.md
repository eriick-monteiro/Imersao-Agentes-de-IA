# Imersão Agentes de IA - Alura + Google Gemini
Este projeto foi desenvolvido durante a [Imersão Agentes de IA](https://cursos.alura.com.br/imersao/imersao-agentes-ia-google), promovida pela Alura em parceria com o Google Gemini.  
Foram três aulas gratuitas com foco em **criação de agentes de IA**, boas práticas e aplicação prática. Ao final, os participantes receberam um **certificado de conclusão**.

## 🛠️ Tecnologias Utilizadas
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

### 📂 Estrutura do Projeto
```bash
📂 projeto-agentes-ia/
├── 📓 notebooks/
│   └── 📓 Imersão_Agentes_de_IA_Alura_+_Google_Gemini
├── 🙈 .gitignore
├── 📖 README.md
└── 📜 requirements.txt
```

## 🚀 Como rodar o projeto (Localmente fora do [Google Colab](http://colab.new/))
### ✅ Pré-requisitos
- Python 3.9 ou superior
- pip instalado
- Conta no [Google AI Studio](https://aistudio.google.com/) para gerar sua GEMINI_API_KEY

### Onde obter a Chave de API
Você pode gerar sua chave gratuita em:  
👉 [Google AI Studio](https://aistudio.google.com/app/apikey)  

### 1. Clone este repositório
```bash
git clone https://github.com/eriick-monteiro/Imersao-Agentes-de-IA.git

# Acessando o diretório
cd projeto-ia
```

### 2. Crie e ative um ambiente virtual
```bash
python -m venv venv

# Linux/Mac
source venv/bin/activate

# Windows
venv\Scripts\activate
```

### 3. Instale as dependências
```bash
pip install -r requirements.txt
```

### 4. Criar e Configurar o seu `.env` com o seguinte conteúdo:
```bash
GEMINI_API_KEY=sua_chave_aqui
```

### 5. Alterar ./notebooks/Imersão_Agentes_de_IA_Alura_+_Google_Gemini.ipynb

De:
```python
from google.colab import userdata
from langchain_google_genai import ChatGoogleGenerativeAI

GOOGLE_API_KEY = userdata.get('GEMINI_API_KEY')
```

Para:
```python
import os
from dotenv import load_dotenv

load_dotenv()
GOOGLE_API_KEY = os.getenv("GEMINI_API_KEY")
```

Assim ele irá pegar a Chave de API no `.env` e estará tudo pronto para rodar projeto

### 6. Execute o Jupyter Notebook
```bash
jupyter notebook
```