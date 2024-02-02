<div align="center">
  <img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Power-Bi-Logo-PNG.png" width="250" height = "150">
</div>

## Descrição
- Relatório de performance e produtividade de lojas de produtos de departamento.
- Performance and productivity report for department stores.

## Projetos
<table>
  <tr>
    <td><img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Dash%20de%20Vendas/Dash%20Vendas%20-%20Power%20BI%20-%20Opera%202024-02-01%2021-18-37%20(online-video-cutter.com).gif" width="400" alt="Imagem"></td>
    <td>
      <h2><a href="https://github.com/Raii-Azevedo/ProjetosBI/tree/master/Dash%20de%20Vendas">Relatório de Vendas</a></h2>
      <p>Dashboard relatório do desempenho de vandas de uma loja.</p>
    </td>
  </tr>
</table>

<div align="center">
## Composição
- Dados de base financeira excel
- Power BI

[![Watch the video]()](https://www.youtube.com/watch?v=jX9NHLga8Mo&list=PLPVMTPUt4GQHa1BeAGUKJrq0Q5UNK_UVv&index=4)
</div>

## Realização
    - Cálcudos de DESPESAS = - CALCULATE(SUM('Movimentações'[Valor da Movimentação]), 'Movimentações'[Tipo] = "Pagamento"
    - Cálculos de MARGEM = [Lucro] / [Receita]
    - Cálculos de MARGEM AUXILIAR = 1 - 'Movimentações'[Margem]
    - Cálculos de DESVIO DE META = [Margem] - 0.3 (30%)
    - Cálculos de IMPOSTO = [Receita] * 0.15 (15%)
    - Cálculos de LUCRO = [Receita] - [Despesas] - 'Movimentações'[Imposto]
    - Cálculos de MOVIMENTAÇÕES PIX = CALCULATE(COUNTROWS('Movimentações'), 'Movimentações'[Forma Pagamento] = "PIX")
    - Cálculos de % PIX= 'Movimentações'[Movimentações Pix] / [Qts Movimentações]
    - Cálculos de PAGAMENTO = CALCULATE(SUM('Movimentações'[Valor da Movimentação]),'Movimentações'[Tipo] = "Pagamento")
    - Cálculos de QTD DE MOVIMENTAÇÕES = COUNTROWS('Movimentações')
    - Cálculos de RECEITA = CALCULATE(SUM('Movimentações'[Valor da Movimentação]), 'Movimentações'[Tipo] = "Recebimento")

  ### Let's connect? 🤝
  <div>
    <p align="center">
      <a href="https://www.linkedin.com/in/raissa-azevedo-555893120/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
      <a href="https://www.instagram.com/raiissa.azevedo/"><img src="https://img.shields.io/badge/-Instagram-E4405F?style=flat&logo=instagram&logoColor=white"/></a>
  </p> </div></div>
</div>
