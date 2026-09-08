# Mini-Projeto Avaliativo: Análise Exploratória de Dados (Base Varejo)
**Turma:** Analise_de_Dados_T6  
**Aluno:** Diego O C Nogueira

## 📌 Descrição do Projeto
Este projeto realiza uma Análise Exploratória de Dados (AED) em uma base de transações de varejo. O objetivo principal é tratar problemas de qualidade de dados (nulos, duplicatas, tipos incorretos) e gerar estatísticas descritivas e agrupamentos para responder perguntas operacionais de negócio.

## 🛠️ Tecnologias Utilizadas
- **Linguagem:** Python 3.x
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Kagglehub
- **Ambiente:** Google Colab / VS Code

## 🔄 Passos da Análise (Sprints)
1. **Sprint 1 - Importação e AED Inicial:** Carregamento automático da base via `kagglehub` e inspeção das dimensões e tipos.
2. **Sprint 2 - Padronização:** Remoção de espaços extras em strings e conversão da coluna de data para `datetime`.
3. **Sprint 3 - Limpeza de Nulos e Duplicatas:** Tratamento da string `#N/D` com substituição por 'Sem Categoria', remoção de colunas vazias e eliminação de duplicatas exatas. Validação da regra do `CO_ID`.
4. **Sprint 4 - Estatística Descritiva:** Cálculo de média, mediana, moda, desvio padrão, quartis e extremos da coluna de número de filhos dos clientes (`CL_FHL`).
5. **Sprint 5 - Agrupamentos:** Construção de tabelas de frequência e visões consolidadas com `groupby()` e `crosstab()`.
6. **Sprint 6 - Visualização:** Geração de gráficos com `seaborn` e `matplotlib` para suporte visual.

## 💡 Principais Conclusões
- Cada linha representa um **item vendido**, enquanto o `CO_ID` representa o carrinho de compras completo.
- Os produtos sem categoria no sistema de origem foram identificados e rotulados como 'Sem Categoria', preservando o histórico de vendas.
- Foram identificadas e removidas duplicatas idênticas geradas por falhas de exportação.

## 🚀 Como Executar
1. Abra o arquivo `.py` ou o notebook no **Google Colab** ou **VS Code**.
2. Certifique-se de ter as bibliotecas instaladas: `pip install pandas matplotlib seaborn kagglehub`.
3. Execute todas as células sequencialmente.
