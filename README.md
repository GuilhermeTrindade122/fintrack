# FinTrack

**Protótipo web para explorar dados financeiros com Python.**

Aplicação Flask com páginas para upload de CSV e dashboard, acompanhada de rotinas iniciais de tratamento de dados e visualização.

## O que existe hoje

- Rotas web para página inicial, upload e dashboard.
- Recebimento de arquivos CSV pela interface.
- Rotina inicial de limpeza com pandas: remoção de duplicatas e valores ausentes, conversão de datas e valores e normalização de campos de texto.
- Função de visualização de matriz de correlação com matplotlib e seaborn.

## Stack

Python · Flask · Jinja · pandas · matplotlib · seaborn · HTML · CSS

## Organização

- [`run.py`](run.py) — ponto de entrada.
- [`app/routes.py`](app/routes.py) — navegação e upload.
- [`app/templates`](app/templates) — páginas da interface.
- [`app/utils/etl.py`](app/utils/etl.py) — tratamento de dados.
- [`app/utils/visualizations.py`](app/utils/visualizations.py) — visualização.
- [`requirements.txt`](requirements.txt) — dependências declaradas.

## Dados esperados pelo ETL

A rotina de tratamento usa as colunas `date`, `amount`, `description` e `category`. O recebimento do arquivo pela interface ainda não conecta automaticamente essa rotina ao dashboard.

## Execução e estágio atual

O ponto de entrada é `python run.py`. Antes de executá-lo, é necessário preparar o ambiente Python e a pasta `uploads` usada pelas rotas.

O arquivo de dependências declara duas versões diferentes de `Flask-WTF`; essa configuração precisa ser resolvida para uma instalação reproduzível. O dashboard e a integração entre upload, tratamento e gráficos permanecem em desenvolvimento.

O repositório registra a construção de uma aplicação de dados, com espaço para evoluir o pipeline e a apresentação dos resultados.
