# Classificação de Cancro do Pulmão com Dados de Tomografia Computorizada (CT)

### Laboratório de Inteligência Artificial e Ciência de Dados  
### Projeto 1 — 2025 / 2026  

---

## Introdução

Este projeto foi desenvolvido no âmbito da unidade curricular **Laboratório de Inteligência Artificial e Ciência de Dados (Lab IA & DC)**.  
O principal objetivo desta UC é proporcionar aos estudantes uma experiência prática na aplicação de **metodologias de desenvolvimento de software**, **técnicas de Inteligência Artificial (IA)** e **Ciência de Dados (CD)**, promovendo o **trabalho em equipa** e a **comunicação científica**.  

No primeiro projeto, o desafio proposto consistiu na **classificação de cancro do pulmão com base em dados de Tomografia Computorizada (CT)**.  
O trabalho envolveu várias fases — desde a **compreensão dos dados**, **pré-processamento** e **seleção de *features***, até à **modelação** e **avaliação de desempenho** — com o objetivo de desenvolver um sistema de apoio ao diagnóstico capaz de distinguir nódulos **benignos** e **malignos** em imagens médicas.  

A base de dados utilizada foi a **LIDC-IDRI (Lung Image Database Consortium – Image Database Resource Initiative)**, uma coleção pública que inclui **1018 estudos de CT torácicos** com anotações de **quatro radiologistas experientes**, amplamente utilizada em investigação de diagnóstico assistido por computador (*Computer-Aided Diagnosis – CAD*).

---

## Estrutura do Projeto

### Notebook Principal
- **`final.ipynb`** — Contém todo o processo do projeto, incluindo:
  - Análise e compreensão dos dados (CT, XML e tabelas);
  - Pré-processamento e limpeza dos dados;
  - Extração de *features* radiômicas e profundas;
  - Seleção de *features* (técnicas estatísticas, PCA e Random Forest);
  - Treino e avaliação de modelos de classificação;
  - Interpretação dos resultados e conclusões.

---

### Pastas e Ficheiros Relevantes

- **`dataset/`**  
  Contém os dados originais fornecidos, nomeadamente:
  - `manifest-1600709154662/LIDC-IDRI/` — estudos de CT em formato DICOM;
  - `tcia-lidc-xml/` — ficheiros XML com anotações dos radiologistas;
  - `lidc-idri-nodule-counts.xlsx` — contagem e caracterização de nódulos;
  - `tcia-diagnosis-data.xls` — diagnósticos de pacientes e métodos clínicos.

- **`radiomic_resume_fixed.csv`**  
  Ficheiro resultante da extração de *features* radiômicas e profundas, utilizado como base para análise.

- **`dataset_clean.csv`**  
  Versão limpa do conjunto de dados, após remoção de valores inválidos e variáveis de fuga (*leakage*).

- **`dataset_prefilter.csv`**  
  Conjunto de dados após filtragem inicial (*label-agnostic prefilter*), com imputação, remoção de variância nula e alta correlação.

- **`selected_FULL__*.csv`**  
  Diferentes versões do dataset após aplicação dos métodos de seleção de *features* (SelectKBest, Random Forest, PCA e baseline).

- **`results/`**  
  Resultados dos modelos avaliados com *cross-validation* e *hold-out testing*, incluindo métricas de desempenho (ROC AUC, F1, Recall e Accuracy).

- **`README.md`**  
  Documento descritivo do projeto (este ficheiro).

- **`ethical_legal_considerations.pdf`**  
  Documento que aborda as implicações éticas e legais da utilização de dados médicos.

---

