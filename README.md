# PyAnalytics: Análise e Engenharia de Dados em Saúde 📊🏥

Universidade Federal de Santa Catarina (UFSC)  — 2026.1

Este repositório foi criado para centralizar e documentar o desenvolvimento das minhas atividades práticas e o projeto final do curso **PyAnalytics - Resolução de Problemas de Análise de Dados e Compartilhamento de Conhecimentos** , realizado no primeiro semestre de 2026 na UFSC.

O objetivo principal é aplicar a linguagem Python e suas principais bibliotecas de Data Science para extrair, tratar, analisar e visualizar dados reais, com foco no ecossistema de Saúde Pública.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

O ecossistema técnico do projeto foi construído utilizando as seguintes ferramentas:

* **Linguagem Base:** Python 3.x
* **Manipulação e Análise de Dados:** `pandas` e `numpy`
* **Visualização de Dados:** `matplotlib` e `seaborn`
* 
**Coleta de Dados e APIs:** `requests` 


* 
**Extração de Dados Não Estruturados:** `pdfplumber` 


* 
**Segurança:** Gerenciador de *Secrets* do Google Colab (`userdata`) 



---

## 📝 Conteúdo dos Projetos

### 🔹 Atividade Prática 1: Desvendando APIs com Python e Dados de Saúde

* 
**Objetivo:** Introduzir o conceito de APIs e demonstrar o consumo de dados reais de órgãos governamentais na área da Saúde Pública.


* 
**Desenvolvimento:** * Autenticação realizada através da configuração do cabeçalho (*headers*) da requisição com o token credencial.


* Consumo de dados de ocupação hospitalar utilizando a biblioteca `requests` para buscar as informações diretamente do DataSUS.


* Tratamento de dados convertendo a resposta do servidor para o formato JSON e, sequencialmente, para um DataFrame do Pandas.


* Execução de limpeza, filtragem e plotagem de gráficos para análise visual das informações extraídas.





### 🔹 Atividade Prática 2: Segurança, Extração de PDFs e Desafio REMUME

* 
**Objetivo:** Garantir a segurança de credenciais de acesso e manipular dados não estruturados comuns na área da saúde.


* **Desenvolvimento:**
* Configuração de token de API de forma segura utilizando o gerenciador de *Secrets* (`userdata`) do Google Colab, evitando chaves expostas diretamente no código.


* Uso da biblioteca `pdfplumber` para acessar, ler e extrair tabelas de medicamentos do documento da REMUME (Relação Municipal de Medicamentos Essenciais).


* Estruturação dos dados extraídos em tabelas limpas e tratamento preventivo de linhas vazias para conversão em uma base utilizável.





### 🏆 Projeto Final: Análise de Ocupação de Leitos Hospitalares (Araranguá/SC)

* 
**Objetivo:** Executar um projeto individual de análise de dados focado em dados regionais de uma base pública de saúde de escolha do aluno.


* **Desenvolvimento:**
* **Carga de Dados:** Carga inicial do dataset de Ocupação de Leitos Hospitalares (base pública ESUS-VEPI), isolando colunas específicas de interesse para otimização de memória.
* **Análise Exploratória e Limpeza:** Identificação de inconformidades nos tipos de dados (datas em formato de texto), conversão temporal estruturada e aplicação de preenchimento de dados faltantes com substituição por zero (`fillna(0)`).
* **Operações com Pandas e NumPy:** Agrupamento de registros diários em médias mensais (`groupby`) e consolidação de estatísticas acumuladas de óbitos com suporte matemático de alta performance.
* **Visualização e Insights:** Geração de gráfico de tendências temporais customizado, evidenciando analiticamente a retração da pressão hospitalar e a redução dos índices de ocupação de UTI para zero no segundo semestre do período analisado.



---

## 👩‍💻 Autoria e Agradecimentos

* **Desenvolvido por:** Esther de Oliveira
* 
**Instituição:** Universidade Federal de Santa Catarina (UFSC) 
---

*README atualizado em 2026.*
