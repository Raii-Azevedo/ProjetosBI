<div align="center">
  <img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Power-Bi-Logo-PNG.png" width="250" height = "150">
</div>

## Descrição
- Relatório de performance fiscal de lojas de produtos eletrônicos ao redor do mundo.
- Sales performance report for electronics stores around the world.

## Projetos
<table>
  <tr>
    <td><img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Relatório%20Elétro/EletroStore.gif" width="400" alt="Imagem"></td>
    <td>
      <h2><a href="https://github.com/Raii-Azevedo/ProjetosBI/tree/master/Relatório%20Elétro">Relatório Bancos</a></h2>
      <p>Relatório de performance fiscal de lojas de produtos eletrônicos ao redor do mundo.</p>
    </td>
  </tr>
</table>

## Composição
- Dados de base financeira CSV
- Power BI


## Realização
    - Cálcudos de Total Venda = SUMX(BaseVendas, BaseVendas[Preço Unitario] * BaseVendas[Quantidade Vendida])
    - Cálculos de Total Venda Ano Anterior = CALCULATE([Total Venda], SAMEPERIODLASTYEAR(Calendario[Datas])
    - Cálculos de Total Venda Variação = DIVIDE( [Total Venda] -  [Total Venda Ano Anterior], [Total Venda Ano Anterior])
    - MÉTRICAS:
        - 1. Contexto = 
        VAR vContexto = SELECTEDVALUE(Metrica[Metrica])
        RETURN 
          SWITCH(
              TRUE(),
              vContexto = "Anterior", [Total Venda Ano Anterior],
              vContexto = "Atual", [Total Venda]
        )

  ### Let's connect? 🤝
  <div>
    <p align="center">
      <a href="https://www.linkedin.com/in/raissa-azevedo-555893120/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
      <a href="https://twitter.com/Raiissa_Azevedo"><img src="https://img.shields.io/badge/-Twitter-%231DA1F2?style=flat&logo=twitter&logoColor=white"/></a>
      <a href="https://www.instagram.com/raiissa.azevedo/"><img src="https://img.shields.io/badge/-Instagram-E4405F?style=flat&logo=instagram&logoColor=white"/></a>
  </p> </div></div>
</div>
