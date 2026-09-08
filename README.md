# Mini-Projeto Avaliativo: Análise Exploratória de Dados (Base Varejo)

**Turma:** Analise_de_Dados_T6  
**Aluno:** Diego O C Nogueira  

---

## 📌 Descrição do Projeto
Este projeto realiza uma Análise Exploratória de Dados (AED) em uma base de transações de varejo. O objetivo principal é tratar problemas de qualidade de dados (nulos, duplicatas, tipos incorretos) e gerar estatísticas descritivas e agrupamentos para responder perguntas operacionais de negócio.

---

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3.x
* **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Kagglehub
* **Ambiente:** Google Colab / VS Code

---

## 🔄 Passos da Análise (Sprints & Histórico de Commits)

O projeto foi construído e versionado incrementalmente no GitHub através dos seguintes commits:

* **Sprint 1 - Importação e AED Inicial:**  
  * *Commit:* `sprint 1: importacao da base de dados do kaggle e analise exploratoria inicial`  
  * Carregamento automático do dataset via `kagglehub` e inspeção das dimensões, colunas e tipos de dados.
* **Sprint 2 - Padronização:**  
  * *Commit:* `sprint 2: padronizacao de texto, conversao numerica e tratamento da data para datetime`  
  * Remoção de espaços em branco extras em strings (`.str.strip()`), ajuste de formatos numéricos e conversão da coluna de data para o tipo `datetime`.
* **Sprint 3 - Limpeza de Nulos e Duplicatas:**  
  * *Commit:* `sprint 3: tratamento de nulos (#N/D), remocao de duplicatas e validacao da regra do co_id`  
  * Substituição de valores nulos e da inconsistência `#N/D` por 'Sem Categoria', eliminação de colunas de exportação vazias (`Unnamed`) e remoção de duplicatas exatas. Validação do papel do `CO_ID`.
* **Sprint 4 - Estatística Descritiva:**  
  * *Commit:* `sprint 4: calculo de medidas estatisticas para a coluna de filhos do cliente (cl_fhl)`  
  * Cálculo das medidas de tendência central e dispersão (média, mediana, moda, desvio padrão, quartis e extremos) para a coluna `CL_FHL`.
* **Sprint 5 - Agrupamentos e Tabelas Cruzadas:**  
  * *Commit:* `sprint 5: agrupamento de dados com groupby e criacao de tabela cruzada`  
  * Construção de tabelas de frequência e visões consolidadas utilizando `groupby()` e `crosstab()`.
* **Sprint 6 - Visualização e Exportação:**  
  * *Commit:* `sprint 6: geracao de graficos para analise visual e relatorio final de conclusoes`  
  * Geração de gráficos com `seaborn` e `matplotlib` para suporte visual e exportação da base final limpa.

---

## 💡 Principais Conclusões e Insights
1. **Granularidade da Base:** Cada linha representa a venda de um item individual, enquanto a coluna `CO_ID` agrupa múltiplos produtos pertencentes ao mesmo carrinho/pedido.
2. **Integridade de Vendas:** Produtos sem categoria cadastrada no ERP de origem (`#N/D` ou nulos) foram rotulados como 'Sem Categoria', garantindo que o faturamento e o histórico total de vendas não fossem descartados.
3. **Limpeza de Ruídos:** Foram identificadas e eliminadas duplicatas idênticas decorrentes de falhas de exportação do sistema.
4. **Perfil do Cliente:** A análise descritiva da coluna `CL_FHL` e o cruzamento com variáveis de gênero e segmento permitiram compreender a distribuição demográfica dos compradores.
5. **Desempenho de Categorias:** O agrupamento por categoria permitiu ranquear os produtos com maior volume de saída e destacar gargalos no cadastro do ERP.

---

## 🧠 Reflexão Teórica: A Importância do ETL e da Qualidade de Dados
O processo de **ETL (Extração, Transformação e Carga)** é a espinha dorsal de qualquer arquitetura de Analytics e Business Intelligence. Dados brutos oriundos de sistemas operacionais frequentemente contêm ruídos, falhas de digitação, valores ausentes e inconsistências que, se não tratados, distorcem os indicadores do negócio. 

Neste projeto, a etapa de **Transformação** permitiu garantir que análises estatísticas não fossem enviesadas por linhas duplicadas e que o histórico financeiro fosse preservado ao imputar o rótulo 'Sem Categoria' em vez de deletar registros. Tratar a qualidade dos dados na origem garante confiabilidade e segurança às tomadas de decisão estratégicas.

---

## 📂 Base Tratada (`df_limpo.rar`)
Devido ao limite rígido de tamanho para uploads via interface web do GitHub (máximo de 25 MB por arquivo), a base de dados tratada final (`df_limpo.csv` com aproximadamente 36 MB) foi compactada e disponibilizada no repositório através do arquivo **`df_limpo.rar`**.

---

## 🚀 Como Executar
1. Clone ou baixe este repositório.
2. Certifique-se de ter o Python 3.x instalado.
3. Instale as dependências do projeto executando o comando no terminal:
   ```bash
   pip install -r requirements.txt
