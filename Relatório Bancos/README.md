<div align="center">
  <img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Power-Bi-Logo-PNG.png" width="250" height = "150">
</div>

## Descrição
- Relatório de performance e produtividade dos bancos mais populares do Brasil, com histórico mês a mês de superavit e déficts.
- Performance and productivity report of the most popular banks in Brazil, with a month-by-month history of surpluses and deficits.

## Projetos
<table>
  <tr>
    <td><img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Relatório%20Bancos/Relatório%20Bancos.gif" width="400" alt="Imagem"></td>
    <td>
      <h2><a href="https://github.com/Raii-Azevedo/ProjetosBI/tree/master/Relatório%20Bancos">Relatório Bancos</a></h2>
      <p>Dashboard relatório do desenvolvimento fiscal dos principais bancos operantes no Brasil.</p>
    </td>
  </tr>
</table>

## Composição
- Dados de base financeira excel
- Power BI

<div align="center">
  [![Watch the video](https://i.stack.imgur.com/Vp2cE.png)](https://www.youtube.com/watch?v=kXHJV3o7ovU&list=PLPVMTPUt4GQHa1BeAGUKJrq0Q5UNK_UVv&index=2)
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
      <a href="https://twitter.com/Raiissa_Azevedo"><img src="https://img.shields.io/badge/-Twitter-%231DA1F2?style=flat&logo=twitter&logoColor=white"/></a>
      <a href="https://www.instagram.com/raiissa.azevedo/"><img src="https://img.shields.io/badge/-Instagram-E4405F?style=flat&logo=instagram&logoColor=white"/></a>
  </p> </div></div>
</div>
