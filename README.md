# 📊 Focus Automation - LIMFIE

Este projeto consiste em uma automação desenvolvida em Python para coletar, tratar e distribuir as expectativas de mercado do **Boletim Focus (Banco Central do Brasil)** para os membros e associados da Liga de Mercado Financeiro do Instituto de Economia da UFRJ (LIMFIE).

A ferramenta otimiza o fluxo de análise macroeconômica ao transformar dados brutos da API do BCB em relatórios visuais gerados e enviados por e-mail de forma 100% automatizada.

## 🚀 Funcionalidades

* **Coleta Automatizada:** Integração com a API de Expectativas de Mercado do Banco Central do Brasil utilizando a biblioteca `bcb`.
* **Análise Comparativa Semanal:** Cálculo de variação (alta `↑`, baixa `↓` ou estabilidade `=`) das médias e medianas dos principais indicadores (IPCA, Câmbio, Selic, PIB, Dívida Líquida, etc.) em relação à semana anterior.
* **Data Vis & Estilização:** * Geração de tabelas de dados estilizadas condicionalmente (azul para alta, vermelho para baixa).
    * Plotagem de gráficos de linha dinâmicos com `Seaborn` e `Matplotlib` mostrando a evolução temporal das projeções para os anos de 2025, 2026 e 2027.
* **Disparo de E-mails (SMTP):** Montagem de e-mail marketing corporativo em HTML com as imagens da tabela e dos gráficos embutidos diretamente no corpo do texto (`MIME/inline`), enviado de forma segura via protocolo SSL para múltiplos destinatários.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Análise de Dados:** `pandas`, `numpy`
* **Coleta de Dados:** `bcb` (Python API para o Banco Central)
* **Visualização de Dados:** `matplotlib`, `seaborn`, `dataframe_image`
* **Comunicação:** `smtplib`, `ssl`, `email` (Módulos nativos para envio de e-mails)

## 📋 Pré-requisitos

Antes de rodar o script, certifique-se de instalar as dependências necessárias:

```bash
pip install pandas numpy matplotlib seaborn bcb dataframe_image
