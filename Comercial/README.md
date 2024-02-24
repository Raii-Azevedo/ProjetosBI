<div align="center">
  <img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Power-Bi-Logo-PNG.png" width="250" height = "150">
</div>

## Descrição
- Dashboard relatório de performance de vendas de colaboradores de loja de eletronicos
- Sales performance dashboard of employees of an eletronic gadget store.
  
## Projetos
<table>
  <tr>
    <td><img src="https://github.com/Raii-Azevedo/ProjetosBI/blob/master/Relatório%20Bancos/Relatório%20Bancos.gif" width="400" alt="Imagem"></td>
    <td>
      <h2><a href="https://github.com/Raii-Azevedo/ProjetosBI/tree/master/Relatório%20Bancos">Relatório Comercial</a></h2>
      <p>Dashboard relatório de performance de vendas de colaboradores de loja de eletronicos</p>
    </td>
  </tr>
</table>

<div align="center">
## Composição
- Dados de base de vendas EXCEL
- Power BI
- HTML
- CSS
- DAX

[![Watch the video]()](https://www.youtube.com/watch?v=HIfrFNRYZ-Y)
</div>


    - % F## Realizaçãouncionários fecharam contrato = [QTD Funcionários Fecharam Contrato] / [QTD Funcionários]
    -  % Meta = DIVIDE([Faturamento Total],[META]) * 100
    -  % Vendas Boleto = DIVIDE([Vendas Boleto],[TOTAL DE VENDAS], "Sem Vendas")
    -  % Vendas Cartão = DIVIDE([Vendas Cartão],[TOTAL DE VENDAS], "Sem Vendas")
    -  Faturamento MTD = TOTALMTD([Faturamento Total],'dCalendário'[Datas])
    -  Faturamento Total = SUMX('Base',Base[Quantidade Vendida] * Base[Valor Unitario])
    -  Lucro Total = SUMX(Base,(Base[Quantidade Vendida] * Base[Valor Unitario]) * 0.9)
    - Maior Cliente = CALCULATE(MAX('Cadastro Cliente'[Cliente]), TOPN(1, ALL('Cadastro Cliente'[Cliente]), [FATURAMENTO TOTAL Serv]))
    - QTD Contratos = COUNT('Serviços Prestados'[Data da Contratação])
    - SALARIO área Adminstrativa = CALCULATE(SUM(CadastroFuncionarios[Salatio Total]), 'Cadastro Cargos'[Área] = "Administrativo")
    - Ticket Médio Contratos = AVERAGE('Cadastro Cliente'[Valor Contrato Anual])
    - Vendas Boleto = CALCULATE([TOTAL DE VENDAS],Base[Forma de Pagamento] = "Boleto")

## CONFIG IMAGEM HTML CSS
        - Imagem borda animada = 
            VAR vImagem_vendedor = 
                SELECTEDVALUE(Base[Imagem Vendedor])

            VAR vPorcentagem = MEDIDAS[% Meta]

            VAR vBorda_cor = 
                SWITCH(
                    TRUE(),
                    vPorcentagem >= 1, "#22FD30", // Acima de 100%
                    vPorcentagem >= 0.8, "#DFEA08", // Acima de 80 %
                    TRUE(),"#CD0E17" // Não atingiu a meta
                )

            VAR vBorda_Espessura = 5

        RETURN
        "
            <style>
                .contorno{
                    position: relative;
                    width: 100vw;
                    height: 100vh;

                    border: 1px solid #3C596BE;
                    border-radius: 10px;

                    display: flex;
                    justify-content: center;
                    align-items: center;
                    overflow: hidden
                }

                .bg {
                    position: absolute;
                    inset: " & vBorda_Espessura & "px;
                    background: #253440;
                    border-radius: 10px
                }

                img {
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    object-fit: contain
                }

                .borda{
                    position: absolute;
                    width: 30%;
                    height: 200%;
                    background: " & vBorda_cor & ";
                    animation: anima-borda 2.5s linear infinite
                }

                @keyframes anima-borda {
                    from {
                        transform: rotate(0)
                    }

                    to {
                        transform: rotate(360deg)
                    }
                }
            </style>

            <div class='contorno'> 
                <div class='borda'>

                </div>
                <div class='bg'>
                    <img src = '" & vImagem_vendedor & "'>
                </div>

            </div>

  ### Let's connect? 🤝
  <div>
    <p align="center">
      <a href="https://www.linkedin.com/in/raissa-azevedo-555893120/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
      <a href="https://twitter.com/Raiissa_Azevedo"><img src="https://img.shields.io/badge/-Twitter-%231DA1F2?style=flat&logo=twitter&logoColor=white"/></a>
      <a href="https://www.instagram.com/raiissa.azevedo/"><img src="https://img.shields.io/badge/-Instagram-E4405F?style=flat&logo=instagram&logoColor=white"/></a>
  </p> </div></div>
</div>
