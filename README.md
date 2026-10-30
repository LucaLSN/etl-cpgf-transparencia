# 🏛️ Pipeline ETL de Despesas Públicas (CPGF)

<div align="center">

  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Processing-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Git-Version%20Control-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
  <img src="https://img.shields.io/badge/Status-Conclu%C3%ADdo-success?style=for-the-badge" alt="Status">

</div>

> Pipeline de Engenharia de Dados desenvolvido para extrair, transformar e carregar (ETL) dados de despesas públicas do Cartão de Pagamento do Governo Federal (CPGF), automatizando o fluxo de auditoria e análise financeira.

---

## 🎯 Sobre o Projeto

Este projeto tem como objetivo automatizar o processamento de dados abertos governamentais, eliminando o trabalho manual de auditoria em planilhas e centralizando as informações em um banco de dados relacional robusto. A solução simula um cenário real de engenharia de dados aplicada ao setor público, aplicando boas práticas de modelagem, tratamento de dados sensíveis e versionamento de código.

---

## 🏗️ Arquitetura do Pipeline (ETL)

O fluxo de dados foi estruturado seguindo o padrão de camadas de Engenharia de Dados:

```text
[ Portal da Transparência (CSV Bruto) ] 
                 │
                 ▼
       📁 data/raw/ (Imutável)
                 │
                 ▼
       🐍 Pandas (Limpeza, Tipagem & Tratamento de Sigilosos)
                 │
                 ▼
       🐘 PostgreSQL (Carga em Banco Relacional / Tabela: despesas_cpgf)
                 │
                 ▼
       📊 DBeaver / Power BI (Análise & Auditoria)
