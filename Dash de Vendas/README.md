<div align="center">
  <img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Power-Bi-Logo-PNG.png" width="250" height = "150">
</div>

## Descrição
- Relatório de performance e produtividade de lojas de produtos de departamento.
- Performance and productivity report for department stores.

## Projetos
<table>
  <tr>
    <td><img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Dash%20de%20Vendas/DASH%20VENDAS.gif" width="400" alt="Imagem"></td>
    <td>
      <h2><a href="https://github.com/Raii-Azevedo/ProjetosBI/tree/master/Dash%20de%20Vendas">Relatório de Vendas</a></h2>
      <p>Dashboard relatório do desempenho de vandas de uma loja.</p>
    </td>
  </tr>
</table>


## Composição
  
  - Dados de base financeira excel
  - Power BI

<div align="center">

[![Watch the video](https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Dash%20de%20Vendas/Youtube%20Capa.png)](https://www.youtube.com/watch?v=jX9NHLga8Mo&list=PLPVMTPUt4GQHa1BeAGUKJrq0Q5UNK_UVv&index=4)
</div>

## Realização
    - Cálculos de % Crescimento Faturamento YoY = var vFat_ano_anterior = CALCULATE(
    [Faturamento Total],
    DATEADD(dCalendario[Datas], -12, MONTH))
    var vCrescimento = DIVIDE([Faturamento Total]- vFat_ano_anterior,vFat_ano_anterior)
    return IF(HASONEVALUE(dCalendario[Ano]) && vcrescimento <> BLANK(),
    vCrescimento,
    "N/A")

    - % Crescimento Lucro YOY = 
    var vLucro_ano_anterior = CALCULATE(
        [Lucro Total],
        DATEADD(dCalendario[Datas], -12, MONTH)
    )
    var vCrescimento = DIVIDE([Lucro Total]- vLucro_ano_anterior,vLucro_ano_anterior)
    return IF(HASONEVALUE(dCalendario[Ano]) && vcrescimento <> BLANK(),
    vCrescimento,
    "N/A")

    - % Crescimento MoM = DIVIDE([Faturamento Total]-[Faturamento Mês Anterior],[Faturamento Mês Anterior],"Sem Histórico")

    - % Crescimento Vendas YoY = 
    var vVendas_ano_anterior = CALCULATE(
        [Total Vendas],
        DATEADD(dCalendario[Datas], -12, MONTH)
    )
    var vCrescimento = DIVIDE(
        [Total Vendas] - vVendas_ano_anterior,
        vVendas_ano_anterior)
    return IF(HASONEVALUE(dCalendario[Ano]) && vcrescimento <> BLANK(),
    vCrescimento,
    "N/A")

    - % Crescimento YoY YTD = 
    IF(HASONEVALUE(dCalendario[Inicio do Mês]),
    DIVIDE(
        [Faturamento YTD]-[Faturamento YTD LY],
        [Faturamento YTD LY]
    ))

    - % Devoluções = [Total Devoluções]/[Total Vendas]

    - % Fat Perdido = [Faturamento Perdido] / [Faturamento Total]

    - % Margem de Lucro = [Lucro Total]/[Faturamento Total]

    - % Vendas (TOP 1 Produto) = 
    [Qtd Vendida (TOP 1 Produto)] / [Total Vendas]

    - % Vendas de Produtos (LOJAS) = 
    [QTD Produtos Vendidos (LOJA)] / [Total Vendas]

    - % Vendas Online = DIVIDE([Vendas Online], [Total Vendas], "Sem vendas")

    - Categoria Selecionada = SELECTEDVALUE(dProdutos[Tipo do Produto], "Selecione uma Categoria")

    - Faturamento LY = 
    var vFaturamentoLY = CALCULATE(
        [Faturamento Total],
        DATEADD(dCalendario[Datas], -1, YEAR)
    )
    return
    IF (HASONEVALUE(dCalendario[Ano]),
    vFaturamentoLY)

    - Faturamento Mês Anterior = CALCULATE(
    [Faturamento Total],
    DATEADD(dCalendario[Datas],-1,MONTH)
    )

    - Faturamento MTD = TOTALMTD([Faturamento Total],dCalendario[Datas])

    - Faturamento Perdido = 
    SUMX(
        'fDevoluções',
        'fDevoluções'[Qtd Devolvida] * RELATED(dProdutos[Preço Unitario])
    )

    - Faturamento QTD = TOTALQTD([Faturamento Total], dCalendario[Datas])

    - Faturamento Total = SUMX(
    fVendas,
    fVendas[Qtd Vendida]*RELATED(dProdutos[Preço Unitario])
    )

    - Faturamento YTD = CALCULATE([Faturamento Total],
    DATESYTD(dCalendario[Datas]))

    - Faturamento YTD 2 = TOTALYTD([Faturamento Total], dCalendario[Datas])

    - Faturamento YTD LY = CALCULATE(
    [Faturamento YTD],
    DATEADD(dCalendario[Datas],-12, MONTH)
    )

    - Lucro Total = SUMX(
    fVendas,
    (fVendas[Qtd Vendida]*RELATED(dProdutos[Preço Unitario]))*0.9-
    fVendas[Qtd Vendida]*RELATED(dProdutos[Custo Unitario])
    )

    - Melhor loja = 
    CALCULATE(MAX(dLojas[Nome da Loja]), 
    TOPN(1, ALL(dLojas[Nome da Loja]), [Total Vendas])
    )

    - Mês selecionado = SELECTEDVALUE(dCalendario[Inicio do Mês], "Selecione um Mês")

    - Prejuízo Devoluções = SUMX(
    'fDevoluções',
    'fDevoluções'[Qtd Devolvida]*RELATED(dProdutos[Preço Unitario])
    )

    - Produto mais vendido = 
    CALCULATE(MAX(dProdutos[Nome Produto]), 
    TOPN(1, ALL(dProdutos[Nome Produto]), [Total Vendas])
    )

    - QTD Produtos Vendidos (LOJA) = 
    CALCULATE(
        [Total Vendas], 
        TOPN(1, ALL(dLojas[Nome da Loja]),
        [Total Vendas])
    )

    - Qtd Vendida (TOP 1 Produto) = 
    CALCULATE(
        [Total Vendas], 
        TOPN(1, ALL(dProdutos[Nome Produto]),
        [Total Vendas])
    )

    - Total Devoluções = SUM('fDevoluções'[Qtd Devolvida])

    - Total Vendas = SUM(fVendas[Qtd Vendida])

    - Vendas Online = CALCULATE(
    [Total Vendas],
    dLojas[Tipo]="Online"
    )

  ### Let's connect? 🤝
  <div>
    <p align="center">
      <a href="https://www.linkedin.com/in/raissa-azevedo-555893120/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
      <a href="https://www.instagram.com/raiissa.azevedo/"><img src="https://img.shields.io/badge/-Instagram-E4405F?style=flat&logo=instagram&logoColor=white"/></a>
  </p> </div></div>
</div>
