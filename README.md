# Projeto Fase 5 – Machine Learning na Cabeça
**Autor:** Kleber Foks – RM 562225  
**Instituição:** FIAP  
**Disciplina:** Inteligência Artificial – Fase 5  

---

## 📌 Contexto
Este projeto faz parte da Fase 5 da disciplina de Inteligência Artificial.  
A atividade consiste em duas entregas obrigatórias:

1. **Entrega 1 – Machine Learning:** análise exploratória dos dados de rendimento agrícola, detecção de outliers, clusterização e criação de cinco modelos preditivos diferentes para prever a produtividade da safra.  
2. **Entrega 2 – Computação em Nuvem (AWS):** estimativa de custos e justificativa técnica para hospedar a solução em nuvem.

Além disso, existem entregas extras opcionais chamadas **“Ir Além”**, que funcionam como desafio de aprofundamento.

---

## 📊 Entrega 1 – Machine Learning
- Dataset utilizado: **`crop_yield.csv`**  
- Técnicas aplicadas:
  - **EDA (Exploratory Data Analysis)**: estatísticas, distribuições, boxplots, correlações, rendimento médio por cultura.  
  - **Outliers**: identificados principalmente no rendimento (`Yield`).  
  - **Clusterização**: K-Means (k=6 sugerido pelo silhouette).  
  - **Modelagem Preditiva**: Linear Regression, Ridge, Lasso, Random Forest e Gradient Boosting.  
  - **Avaliação**: MAE, RMSE, R² e Cross-Validation.  

📈 **Resultados:**  
- Melhor modelo: **Linear Regression**, com **R² ≈ 0.98** e **RMSE ≈ 9.400**.  
- Forte relação linear entre variáveis climáticas e rendimento.  
- Modelo simples, mas altamente explicativo.  

📄 **Notebook completo:**  
👉 [Acesse o notebook no GitHub](./KleberFoks_rm562225_pbl_fase4.ipynb)

🎥 **Vídeo demonstrativo (YouTube, não listado):**  
👉 [Link para o vídeo](COLE_AQUI_O_LINK)

---

## ☁️ Entrega 2 – Computação em Nuvem (AWS)
Nesta entrega foi utilizada a **AWS Pricing Calculator** para estimar os custos de uma máquina Linux simples, com as seguintes configurações:  

- 2 vCPUs  
- 1 GiB RAM  
- Até 5 Gbps de rede  
- 50 GB de armazenamento (HD)  

📌 Comparação realizada entre as regiões:  
- **São Paulo (BR)**  
- **Norte da Virgínia (EUA)**  

### 🔹 Resultados esperados
- A região da **Virgínia do Norte** apresentou custo mais baixo.  
- Contudo, devido a **restrições legais de armazenamento de dados no exterior** e a necessidade de **menor latência**, a opção escolhida foi **São Paulo (BR)**.  

📄 A análise completa, com prints da calculadora, gráficos comparativos e justificativa técnica, está no [README atualizado](./README.md).

🎥 **Vídeo demonstrativo (YouTube, não listado):**  
👉 [Link para o vídeo](COLE_AQUI_O_LINK)

---

## 🏁 Conclusões
- O rendimento agrícola pode ser previsto com **alta precisão** a partir das variáveis climáticas e do tipo de cultura.  
- O modelo linear se mostrou suficiente para explicar os padrões, embora culturas de alto rendimento apresentem maiores erros.  
- A utilização da AWS em São Paulo garante conformidade legal e menor latência, mesmo com custo maior em relação à Virgínia.  

---

## 🚀 Próximos Passos
- Realizar tuning de hiperparâmetros em Random Forest e Gradient Boosting.  
- Ampliar o dataset com variáveis adicionais (solo, fertilização, pragas, índices climáticos).  
- Testar validação temporal para prever safras futuras.  
- Explorar integrações com sensores IoT (Ir Além).
