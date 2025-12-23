# Tech Challenge 4 – Análise de Vídeo com Visão Computacional

## 📌 Descrição do Projeto
Este projeto foi desenvolvido como parte do **Tech Challenge 4** da pós-graduação, com o objetivo de criar uma aplicação de **análise de vídeo** utilizando técnicas de **visão computacional** e **deep learning**.

A aplicação realiza:
- Reconhecimento facial
- Análise de expressões emocionais
- Detecção de atividades
- Identificação de anomalias
- Geração automática de relatório
- Demonstração em vídeo do funcionamento da solução

---

## 👤 Autor
- **Nome:** Luís Felipe Alves Silva  
- Entrega individual – FIAP | Pós IA para Devs  
- RM: 363734
---

## 🎯 Objetivos
- Identificar e marcar rostos presentes em um vídeo
- Classificar emoções faciais detectadas
- Analisar atividades com base no movimento entre frames
- Detectar movimentos anômalos
- Gerar automaticamente um resumo das análises realizadas

---

## 🧠 Tecnologias Utilizadas
- Python 3
- Google Colab
- OpenCV
- InsightFace (detecção facial)
- TensorFlow / Keras
- Modelo de emoções treinado no dataset FER-2013

---

## ⚙️ Funcionamento da Aplicação

### 1. Reconhecimento Facial
Os rostos presentes no vídeo são detectados utilizando a biblioteca **InsightFace**, que é robusta para detecção facial em vídeos reais, inclusive com múltiplas pessoas em cena.

### 2. Análise de Expressões Emocionais
Cada rosto detectado é analisado por um modelo de deep learning treinado no dataset **FER-2013**, classificando as emoções:
- happy
- sad
- angry
- fear
- surprise
- neutral

### 3. Detecção de Atividades
A atividade é classificada frame a frame com base na variação entre frames consecutivos:
- parado
- movimento leve
- movimento intenso

### 4. Detecção de Anomalias
De acordo com o enunciado do desafio, movimentos anômalos são aqueles que não seguem o padrão geral de atividades, como gestos bruscos ou comportamentos atípicos.  
Neste projeto, **anomalias são definidas como frames classificados como movimento intenso**.

### 5. Geração de Relatório
Ao final do processamento, a aplicação gera automaticamente:
- `summary.txt` – relatório em texto
- `summary.json` – relatório em formato estruturado

---

## 📊 Resultados Obtidos

- **Total de frames analisados:** 3326  
- **Total de faces analisadas:** 4452  
- **Número de anomalias detectadas:** 20  

### Distribuição de Atividades
- parado: 2636  
- movimento leve: 670  
- movimento intenso: 20  

### Distribuição de Emoções
- sad: 1283  
- neutral: 516  
- happy: 1129  
- angry: 1137  
- fear: 222  
- surprise: 165  

---

## 🎥 Demonstração em Vídeo
O vídeo de demonstração apresenta:
- Caixas delimitadoras nos rostos detectados
- Emoção predominante exibida acima de cada rosto
- Atividade detectada exibida na parte inferior do vídeo

📺 **Link do vídeo no YouTube:**  
https://youtu.be/hG_JM4McwIA

---

## ▶️ Como Executar o Projeto
1. Abrir o notebook no Google Colab
2. Selecionar ambiente com GPU (recomendado)
3. Executar as células em ordem
4. Fazer upload do vídeo original
5. Aguardar o processamento
6. Baixar os arquivos gerados na pasta `output/`

---

## 📁 Estrutura do Repositório
```
├── notebook.ipynb
├── summary.txt
├── summary.json
└── README.md
```

---

## ✅ Conclusão
O projeto atende integralmente aos requisitos propostos no Tech Challenge 4, integrando técnicas de visão computacional e deep learning para análise de vídeo, com geração automática de resultados e relatório.
