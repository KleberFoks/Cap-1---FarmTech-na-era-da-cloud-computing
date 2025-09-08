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
  - **EDA (Exploratory Data Analysis):** estatísticas, distribuições, boxplots, correlações, rendimento médio por cultura.  
  - **Outliers:** identificados principalmente no rendimento (`Yield`).  
  - **Clusterização:** K-Means (k=6 sugerido pelo silhouette).  
  - **Modelagem Preditiva:** Linear Regression, Ridge, Lasso, Random Forest e Gradient Boosting.  
  - **Avaliação:** MAE, RMSE, R² e Cross-Validation.  

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
- 2 GiB RAM (instância t3.small, mais próxima da configuração solicitada)  
- Até 5 Gbps de rede  
- 50 GB de armazenamento (EBS gp3)  

📌 Comparação realizada entre as regiões:  
- **São Paulo (BR)**  
- **Norte da Virgínia (EUA)**  

### 🔹 Resultados obtidos

| Região             | Instância | vCPUs | Memória | Armazenamento | Preço (USD/mês) |
|--------------------|-----------|-------|---------|---------------|-----------------|
| São Paulo (BR)     | t3.small  | 2     | 2 GiB   | 50 GB GP3     | 32,13           |
| Virgínia do Norte  | t3.small  | 2     | 2 GiB   | 50 GB GP3     | 7,80            |

### 🔹 Justificativa da escolha
Embora a região da **Virgínia do Norte (EUA)** apresente custo significativamente menor (~7,80 USD/mês contra 32,13 USD/mês em São Paulo), a opção adequada é **São Paulo (BR)**, pois:  
- Há **restrições legais** para armazenamento de dados no exterior.  
- Hospedar a API próxima à fazenda garante **menor latência** e melhor tempo de resposta.  
- Assim, mesmo com custo mais elevado, São Paulo é a escolha correta.

📸 Prints da calculadora AWS foram adicionados na pasta `docs/prints_aws` do repositório.  

🎥 **Vídeo demonstrativo (YouTube, não listado):**  
👉 [Link para o vídeo](COLE_AQUI_O_LINK)

---

## 🏁 Conclusões
- O rendimento agrícola pode ser previsto com **alta precisão** a partir das variáveis climáticas e do tipo de cultura.  
- O modelo linear foi suficiente para explicar os padrões, embora culturas de alto rendimento apresentem maiores erros.  
- A utilização da AWS em **São Paulo** garante conformidade legal e menor latência, mesmo com custo maior em relação à Virgínia.  

---

## 🚀 Próximos Passos
- Explorar tuning de hiperparâmetros em Random Forest e Gradient Boosting.  
- Ampliar o dataset com variáveis adicionais (solo, fertilização, pragas, índices climáticos).  
- Avaliar modelos não lineares e validação temporal (safras passadas vs futuras).  
- Integrar a solução com sensores IoT (Ir Além).
