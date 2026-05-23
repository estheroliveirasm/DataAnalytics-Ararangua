# PyAnalytics: Resolução de Problemas de Análise de Dados e Compartilhamento de Conhecimentos

Este repositório armazena o conjunto de projetos estruturados, análises preditivas/exploratórias e pipelines de engenharia de dados desenvolvidos para o ecossistema de Saúde Pública, vinculados à Universidade Federal de Santa Catarina (UFSC).

O objetivo principal deste ecossistema é demonstrar a aplicação prática de bibliotecas Python no consumo de APIs governamentais, na extração de dados tabulares de documentos não estruturados (PDFs) e no desenvolvimento de análises estatísticas regionais baseadas em microdados públicos de saúde.

---

## Estrutura do Repositório

O repositório está organizado em módulos que refletem a evolução técnica do projeto, dividindo-se entre scripts de automação e notebooks de análise avançada:

* **Atividade Prática 1:** Script em Python voltado para a automação de requisições HTTP, consumo de APIs estruturadas e mapeamento da ocupação hospitalar em nível nacional.
* **Atividade Prática 2:** Notebook focado em técnicas de Engenharia de Dados, manipulação de arquivos não estruturados e implementação de protocolos de segurança para credenciais.
* **Projeto Final:** Notebook analítico contendo o estudo de caso detalhado sobre a flutuação e o comportamento da ocupação de leitos hospitalares no município de Araranguá/SC durante o ano de 2022.

---

## Detalhamento Técnico dos Módulos

### 1. Consumo de APIs e Dados do DataSUS (Atividade Prática 1)
* **Objetivo:** Estabelecer uma arquitetura de integração programática com barramentos governamentais para extrair em tempo real indicadores hospitalares de forma dinâmica.
* **Abordagem Técnica:**
  * Implementação da biblioteca `requests` para o consumo do endpoint oficial da API de Dados Abertos do DataSUS (Registro de Ocupação Hospitalar COVID-19).
  * Configuração de segurança via cabeçalhos autenticados (`headers`), injetando chaves de acesso dinâmicas (`chave-api-dados`).
  * Tratamento do payload bruto: conversão de respostas em formato JSON para estruturas tabulares nativas (`pandas.DataFrame`).
  * Saneamento e tipagem de dados: conversão de strings numéricas e agregação volumétrica agrupada por Unidade Federativa (UF).
* **Visualização:** Geração de gráficos estatísticos customizados via `seaborn` e `matplotlib`, ordenando o ranking nacional de registros para facilitar a tomada de decisão assistencial.

### 2. Engenharia de Dados - Extração de PDFs e Segurança (Atividade Prática 2)
* **Objetivo:** Ingerir, tratar e converter dados armazenados em formatos não estruturados (PDFs oficiais) para datasets organizados, mitigando riscos de segurança da informação.
* **Abordagem Técnica:**
  * Uso do gerenciador isolado de ambiente do Google Colab (`google.colab.userdata`) para captura segura de chaves privadas (Secrets), evitando a exposição de tokens no código fonte (*hardcoding*).
  * Implementação de rotinas preventivas de verificação de arquivos locais através do módulo nativo `os`.
  * Utilização da biblioteca `pdfplumber` para a varredura, leitura e extração de matrizes de dados das páginas da Relação Municipal de Medicamentos Essenciais (REMUME 2024).
  * Aplicação de filtros condicionais lógicos para expurgar registros vazios, nulos ou ruidosos gerados pela conversão do PDF.
  * Exportação e persistência de dados em arquivo CSV estruturado utilizando codificação de caracteres `utf-8-sig`, garantindo a integridade ortográfica da língua portuguesa.

### 3. Estudo de Caso Regional: Ocupação de Leitos Hospitalares (Projeto Final)
* **Objetivo:** Avaliar a pressão e o comportamento do sistema de saúde do município de Araranguá/SC ao longo do ano epidemiológico de 2022, utilizando a base de microdados pública do ESUS-VEPI.
* **Abordagem Técnica:**
  * Carga automatizada dos dados de saúde a partir de repositório em nuvem via Google Drive API, restringindo a leitura às colunas críticas para otimização de performance e memória.
  * Normalização temporal: tratamento e conversão do campo de notificações para objetos nativos do tipo `datetime`, seguidos de ordenação cronológica.
  * Limpeza de dados faltantes (*NaN*) utilizando imputação controlada por zero (`fillna(0)`), em total conformidade com a lógica de negócio hospitalar (ausência de registro equivalendo a leitos livres).
  * Execução de cálculos estatísticos complexos e agrupamentos por períodos sazonais através de métodos consolidados do `pandas` e `numpy` (`groupby`, `mean`, `max`, `np.sum`).
* **Principais Insights Gerados:**
  * Mapeamento do estresse assistencial focado no primeiro bimestre de 2022, apresentando picos de até 7 pacientes simultâneos em UTI e um acumulado anual de 15 óbitos na região.
  * Identificação de estabilização absoluta do sistema de saúde local entre os meses de agosto e novembro, registrando média zero de ocupação em leitos críticos, o que evidencia a eficácia das campanhas vacinais e barreiras sanitárias no período.

---

## Tecnologias e Dependências do Ecossistema

* **Python 3:** Linguagem de programação base de todo o ecossistema analítico.
* **Pandas:** Biblioteca de alto desempenho para fatiamento, limpeza, agrupamento e transformação de datasets.
* **NumPy:** Computação científica e processamento vetorial de arrays multidimensionais.
* **Requests:** Cliente HTTP para comunicação e consumo de APIs REST estruturadas.
* **Pdfplumber:** Motor de parsing e extração de texto e tabelas de arquivos PDF.
* **Matplotlib & Seaborn:** Bibliotecas de plotagem de dados para geração de gráficos estatísticos e painéis visuais.
