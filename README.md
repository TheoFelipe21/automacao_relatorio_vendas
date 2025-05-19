# Projeto de Automação de Relatórios de Vendas

Este é um projeto Python, esenvolvido para automatizar o processo de geração e envio de relatórios de vendas para uma rede de lojas. A ideia surgiu da necessidade de otimizar o acompanhamento do desempenho das lojas, fornecendo informações relevantes de forma rápida e eficiente para os gerentes e a diretoria.

## Visão Geral

O projeto consiste em realiza as seguintes tarefas:

1.  **Leitura de Dados:** Importa dados de vendas de diferentes fontes (arquivos CSV e Excel) e informações sobre as lojas e os contatos dos gerentes (arquivos CSV).
2.  **Processamento e Análise:**
    * Unifica os dados de vendas com as informações das lojas para realizar análises específicas por loja.
    * Calcula indicadores de desempenho chave para cada loja, tanto para o dia atual quanto para o acumulado do ano, incluindo:
        * Faturamento total.
        * Diversidade de produtos vendidos.
        * Ticket médio por venda.
    * Compara os indicadores com metas predefinidas para o dia e para o ano.
    * Gera um ranking das lojas com melhor e pior desempenho de faturamento no dia e no ano.
3.  **Geração de Relatórios Visuais:** Cria tabelas de resumo de desempenho diário e anual para cada loja e as salva como imagens (`.png`).
4.  **Backup de Dados:** Salva uma cópia da planilha de vendas de cada loja para o dia analisado em pastas específicas de backup.
5.  **Envio de E-mails:**
    * Envia automaticamente um e-mail para cada gerente de loja contendo:
        * Uma saudação personalizada.
        * Um resumo do desempenho da loja no dia anterior.
        * As tabelas de indicadores de desempenho diário e anual incorporadas como imagens no corpo do e-mail.
        * A planilha de vendas detalhada da loja como um anexo em formato CSV.
    * Envia um e-mail para a diretoria com um resumo do desempenho geral das lojas, incluindo o ranking de faturamento diário e anual, anexado como arquivos CSV.

## Tecnologias Utilizadas

* **Python:** A linguagem de programação principal utilizada para desenvolver o script.
* **Pandas:** Uma biblioteca poderosa para análise e manipulação de dados tabulares.
* **Pathlib:** Um módulo para manipulação de caminhos de arquivos de forma orientada a objetos.
* **Shutil:** Um módulo para operações de arquivo de alto nível (neste caso, para criação de pastas).
* **Dataframe\_image:** Uma biblioteca para exportar DataFrames do Pandas como arquivos de imagem.
* **smtplib e email:** Módulos da biblioteca padrão do Python para envio de e-mails.
* **Threading:** Um módulo para executar tarefas em paralelo (neste projeto, para salvar as imagens das tabelas).

## Dados Utilizados

Para o desenvolvimento e teste deste projeto, foram utilizadas bases de dados simuladas. Os arquivos `Lojas.csv`, `Vendas.xlsx` e `Emails.csv` contêm informações fictícias de lojas, vendas e contatos de gerentes, respectivamente. **Esses dados foram criados exclusivamente para fins de estudo e demonstração da funcionalidade do script de automação e não devem ser interpretados como dados reais.**

## Como Executar o Projeto

1.  **Pré-requisitos:** Certifique-se de ter o Python instalado em seu ambiente. Recomenda-se usar um ambiente virtual para gerenciar as dependências do projeto.
2.  **Instalação das Dependências:**
    ```bash
    pip install pandas pathlib shutil dataframe_image
    ```
3.  **Configuração:**
    * Organize os arquivos de dados (`Lojas.csv`, `Vendas.xlsx`, `Emails.csv`) na pasta `Bases de Dados/`.
    * Crie um arquivo chamado `senha_email.py` na raiz do projeto e defina uma variável `senha_app` com a senha de um "App password" gerado para sua conta Gmail (necessário para o envio de e-mails via Gmail).
    ```

## Aprendizados e Próximos Passos

Com este projeto pude desenvolver minhas habilidade em python como:

* Manipulação e análise de dados com Pandas.
* Automação de tarefas repetitivas.
* Geração de relatórios e visualizações básicas.
* Envio de e-mails programaticamente.
* Organização de arquivos e pastas.

---