## PyAnalytics: Análise e Engenharia de Dados em Saúde 📊🏥

🎓 Universidade Federal de Santa Catarina (UFSC) — 2026.1
Desenvolvido por: Esther Oliveira
Projeto: PyAnalytics

Linha de Pesquisa: Resolução de Problemas de Análise de Dados e Compartilhamento de Conhecimentos

## 🎯 Sobre o Projeto
Este repositório foi meticulosamente desenhado para centralizar a evolução técnica e prática desenvolvida ao longo da jornada PyAnalytics. O core deste ecossistema consiste em aplicar o ecossistema robusto do Python para resolver desafios reais em Saúde Pública, transformando dados brutos ou não estruturados em ativos de informação prontos para o diagnóstico e para a tomada de decisão estratégica.

Toda a infraestrutura lógica e visual do projeto foi sustentada sobre o poder analítico das bibliotecas pandas, numpy, matplotlib, seaborn, requests e pdfplumber, integradas de forma dinâmica ao ambiente do Google Colab.

## 📝 Ecossistema de Atividades Práticas
🔹 Atividade Prática 1: Desvendando APIs com Python e Dados de Saúde
Foco: Consumo de Dados Governamentais e Infraestrutura de APIs

Construção: Introdução conceitual e prática às arquiteturas de API. O pipeline implementou a configuração minuciosa de cabeçalhos HTTP com tokens credenciais para consumir dados reais de ocupação hospitalar de COVID-19 diretamente da API do DataSUS. Os payloads em formato JSON foram estruturados em um DataFrame estruturado, limpando ruídos e gerando um ranking estatístico visual da taxa de ocupação por Unidade Federativa (UF) alimentado pela biblioteca Seaborn.

🔹 Atividade Prática 2: Segurança, Extração de PDFs e Desafio REMUME
Foco: Governança de Credenciais (Security) e Mineração de Dados Não Estruturados

Construção: Uma imersão profunda na segurança de dados em pipelines de engenharia. Utilizando o recurso nativo Colab Secrets, foi desenvolvida uma camada isolada para o carregamento seguro de chaves sensíveis, mitigando riscos de vazamento (hardcoding). Complementarmente, o script utilizou técnicas avançadas com a biblioteca pdfplumber para quebrar a opacidade de documentos textuais, minerando e extraindo tabelas complexas do documento oficial da REMUME 2024 (Relação Municipal de Medicamentos Essenciais) para transformá-las numa base de dados analítica e limpa.

🔹 Atividade Prática 3: Garimpo e Diagnóstico de Dados de Saúde
Foco: Data Auditing, Auditoria de Qualidade e Prontidão de Bases

Construção: Um verdadeiro laboratório de resiliência e tomada de decisão técnica. Após identificar limitações operacionais na API do SINASC, o projeto realizou uma virada ágil para o ecossistema do SISAGUA (População Abastecida). Foi executado um minucioso diagnóstico exploratório focado no mapeamento estrito da integridade dos dados: análise de tipos primitivos, detecção de linhas duplicadas e a geração de um mapa térmico analítico de dados nulos, avaliando o grau de maturidade da base antes de qualquer etapa de modelagem preditiva.

🔹 Atividade Prática 4: Da Exploração ao Insight Territorial
Foco: Paginação Avançada, Data Cleansing e Inteligência Geográfica (Geospatial)

Construção: O ápice do ecossistema analítico. Implementou-se um pipeline robusto capaz de lidar com grandes volumes de dados através do consumo em lotes (paginação com controle de offset/limit) na API nacional de Unidades Básicas de Saúde (UBS), processando uma carga inicial de 15.000 registros. Aplicando filtros geográficos cirúrgicos, a base foi reduzida para espelhar unicamente a malha territorial do estado de Santa Catarina (42) e do município de Araranguá (420140). O projeto respondeu a questões cruciais de negócio voltadas para a futura integração de dashboards no Streamlit, mapeando e distribuindo a densidade da infraestrutura de saúde por bairros com auxílio de coordenadas de latitude e longitude.

🏆 Projeto Final: Análise de Ocupação de Leitos Hospitalares (Araranguá/SC)

Análise exploratória e estatística completa utilizando dados regionais da base pública ESUS-VEPI do ano de 2022. O trabalho envolveu a carga otimizada do dataset focado no município de Araranguá, conversão de datas textuais para o formato temporal correto e tratamento de valores nulos através da substituição por zero (fillna). Foram realizadas operações de agrupamento mensal com Pandas (groupby) e consolidação estatística do total acumulado de óbitos com suporte do NumPy. A análise foi finalizada com um gráfico de linhas customizado no Matplotlib, demonstrando a evolução e a retração da pressão hospitalar na região.

## 👩‍💻 Autora
Esther Oliveira Universidade Federal de Santa Catarina • PyAnalytics 2026/1
