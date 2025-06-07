# 🚀 Sistema de Gerenciamento de Estoque com Análise de Dados

## 📖 Descrição do Projeto

Este projeto é uma aplicação web full-stack desenvolvida em Python com o microframework Flask. O sistema permite o gerenciamento completo do ciclo de vida de produtos em um estoque, incluindo funcionalidades de cadastro, visualização, edição, exclusão e pesquisa.

A aplicação conta com um sistema de autenticação de usuários e controle de acesso baseado em permissões, garantindo que apenas usuários administradores possam gerenciar o estoque.

Além da aplicação web, o projeto inclui um script de análise de dados que lê o banco de dados da aplicação, processa as informações utilizando a biblioteca Pandas e gera visualizações de dados (gráficos) e relatórios tabulares (CSV) com Matplotlib e Seaborn.

---

## ✨ Funcionalidades Principais

- **Autenticação de Usuários:**

  - Cadastro de novos usuários.
  - Login seguro com senhas criptografadas.
  - Controle de acesso baseado em permissões de administrador.

- **Gerenciamento de Produtos (CRUD):**

  - 📝 **Adicionar** novos produtos com detalhes como código, quantidade e datas.
  - 👁️ **Visualizar** todos os produtos em um dashboard paginado e organizado.
  - ✏️ **Editar** as informações de produtos existentes.
  - 🗑️ **Excluir** produtos do sistema.
  - 🔍 **Pesquisar** produtos por nome, código ou descrição.

- **Análise e Visualização de Dados:**
  - 📊 Script independente para gerar relatórios e gráficos a partir dos dados do estoque.
  - Geração de gráficos sobre a distribuição de produtos, cadastros por usuário e evolução ao longo do tempo.
  - Exportação dos dados consolidados para um arquivo `.csv`.

---

## 🛠️ Tecnologias Utilizadas

- **Backend:** Python 3, Flask, SQLAlchemy
- **Frontend:** HTML5, CSS3, Bootstrap 4
- **Banco de Dados:** SQLite
- **Análise de Dados:** Pandas, Matplotlib, Seaborn

---

## 📂 Estrutura do Projeto

O projeto segue o padrão de fábrica (Application Factory) para uma organização modular e escalável.

```
/RAD_StocKing/
|
├── instance/
│   └── estoque.db         # Arquivo do banco de dados (gerado automaticamente)
|
├── static/
│   └── favicon.ico        # Ícone da aplicação
|
├── templates/
│   ├── base.html          # Template base com a estrutura principal e Bootstrap
│   ├── login.html         # Página de login
│   ├── cadastro.html      # Página de cadastro de usuário
│   ├── index.html         # Dashboard principal de gerenciamento de produtos
│   ├── edit.html          # Página para edição de um produto
│   └── no_permission.html # Página de acesso negado
|
├── graficos/
│   ├── grafico_*.png      # Gráficos gerados pelo script de análise
│   └── tabela_produtos.csv# Tabela exportada pelo script de análise
|
├── app.py                 # Ponto de entrada da aplicação (cria a app Flask)
├── db.py                  # Instância do SQLAlchemy
├── models.py              # Definições dos modelos do banco de dados (User, Product)
├── routes.py              # Definição de todas as rotas e lógica da aplicação
├── analise.py             # Script para análise de dados e geração de gráficos
├── requirements.txt       # Lista de dependências Python do projeto
└── .gitignore             # Arquivos e pastas a serem ignorados pelo Git
```

---

## ⚙️ Instalação e Execução

Siga os passos abaixo para executar o projeto em um ambiente local.

**1. Pré-requisitos:**

- Python 3.x instalado.
- Git instalado.

**2. Clone o Repositório:**

```bash
git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git)
cd SEU_REPOSITORIO
```

_(Substitua pela URL do seu repositório)_

**3. Crie e Ative um Ambiente Virtual:**

```bash
# Criar o ambiente virtual
python -m venv env

# Ativar no Windows
.\env\Scripts\activate

# Ativar no macOS/Linux
source env/bin/activate
```

**4. Instale as Dependências:**

```bash
pip install -r requirements.txt
```

**5. Execute a Aplicação Web:**

```bash
python app.py
```

A aplicação estará disponível em `http://127.0.0.1:5000`.

- O primeiro passo é **cadastrar um usuário** marcando a caixa de "Conceder permissão de administrador".
- Em seguida, faça login com este usuário para acessar o dashboard e gerenciar os produtos.
- Os gráficos e o arquivo `.csv` serão salvos na pasta `/relatorios`.

---

## ✒️ Autor

Desenvolvido por **Erick Valente Sprogis - 202403871751**, **Jhonatan Victor Ramos Conde - 202403718774**, **Gustavo Henrique Costa Ribeiro - 202503103011**.
