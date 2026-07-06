# PyAnalytics: Análise e Engenharia de Dados em Saúde 📊🏥

### Universidade Federal de Santa Catarina (UFSC) — 2026.1

Este repositório foi desenvolvido para centralizar as atividades práticas e o projeto final do curso **PyAnalytics - Resolução de Problemas de Análise de Dados e Compartilhamento de Conhecimentos**, realizado no primeiro semestre de 2026 na UFSC. O objetivo principal é aplicar Python e suas principais bibliotecas de Data Science para extrair, tratar e analisar dados reais do ecossistema de Saúde Pública. Toda a base técnica foi construída utilizando as bibliotecas `pandas`, `numpy`, `matplotlib`, `seaborn`, `requests` e `pdfplumber`, integradas ao ambiente do Google Colab.

---

## 📝 Trabalhos Desenvolvidos

### 🔹 Atividade Prática 1: Desvendando APIs com Python e Dados de Saúde

Introdução ao conceito de APIs e ao consumo de dados governamentais. A atividade envolveu a configuração de cabeçalhos de requisição com token credencial para buscar dados de ocupação hospitalar de COVID-19 diretamente da API do DataSUS. Os dados retornados foram convertidos de JSON para um DataFrame do Pandas e, após as etapas de filtragem e limpeza, foi gerado um gráfico de barras com o ranking de ocupação por estado utilizando a biblioteca Seaborn.

### 🔹 Atividade Prática 2: Segurança, Extração de PDFs e Desafio REMUME

Voltada para a governança de credenciais e captura de dados não estruturados na área da saúde. Foi implementado o uso do recurso *Colab Secrets* para carregar chaves de API de forma isolada, evitando a exposição de dados sensíveis diretamente no código. Além disso, utilizou-se a biblioteca `pdfplumber` para acessar, ler e extrair tabelas do documento da REMUME 2024 (Relação Municipal de Medicamentos Essenciais), convertendo informações complexas em uma base de dados limpa e livre de linhas vazias.

### 🏆 Projeto Final: Análise de Ocupação de Leitos Hospitalares (Araranguá/SC)

Análise exploratória e estatística completa utilizando dados regionais da base pública ESUS-VEPI do ano de 2022. O trabalho envolveu a carga otimizada do dataset focado no município de Araranguá, conversão de datas textuais para o formato temporal correto e tratamento de valores nulos através da substituição por zero (`fillna`). Foram realizadas operações de agrupamento mensal com Pandas (`groupby`) e consolidação estatística do total acumulado de óbitos com suporte do NumPy. A análise foi finalizada com um gráfico de linhas customizado no Matplotlib, demonstrando a evolução e a retração da pressão hospitalar na região.

---

## 👩‍💻Autora
Esther Oliveira
Universidade Federal de Santa Catarina • PyAnalytics 2026/1
