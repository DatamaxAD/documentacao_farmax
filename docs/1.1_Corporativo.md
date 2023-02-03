# **Seja bem vindo (a)**

<font size ="2">
**Documentação do dashboard <span style = "color: blue">Corporativo</span>, clique abaixo e navegue para Power BI Service**

<a href="https://app.powerbi.com/links/KA-5DCCH5e?ctid=4019cfa9-aae5-4964-912e-b0e0bb606d37&pbi_source=linkShare" target="_blank">
**BI Corporativo**
</a>


---
<font size ="2">

## **OBJETIVO**
Exibição dos principais indicadores corporativos.

## **FONTE DE DADOS**

1. **obt_sales**
~~~
let
    Fonte = AmazonRedshift.Database("farmax-cluster.cdkgzqhbae0k.us-east-1.redshift.amazonaws.com:5439","farmaxcluster"),
    public = Fonte{[Name="public"]}[Data],
    obt_sales = public{[Name="obt_sales"]}[Data]
~~~

2. **CombustÍveis**
~~~
let
    Fonte = Csv.Document(Web.Contents(" https://www.gov.br/anp/pt-br/centrais-de-conteudo/dados-abertos/arquivos/shpc/qus/ultimas-4-semanas-gasolina-etanol.csv"),
    [Delimiter=";", Columns=16, Encoding=65001, QuoteStyle=QuoteStyle.None])
    
~~~

3. **Marca**
~~~
let
    Fonte = AmazonRedshift.Database("farmax-cluster.cdkgzqhbae0k.us-east-1.redshift.amazonaws.com:5439","farmaxcluster"),
    public = Fonte{[Name="public"]}[Data],
    obt_sales = public{[Name="dim_material"]}[Data]
    
~~~

4. **dim_return**
~~~
let
    Fonte = AmazonRedshift.Database("farmax-cluster.cdkgzqhbae0k.us-east-1.redshift.amazonaws.com:5439","farmaxcluster"),
    public = Fonte{[Name="public"]}[Data],
    dim_return1 = public{[Name="dim_return"]}[Data]
    
~~~

5. **USD**
~~~
let
    Fonte = Web.BrowserContents("https://www.investing.com/currencies/usd-brl-historical-data")
    
~~~

6. **EUR**
~~~
let
    Fonte = Web.BrowserContents("https://www.investing.com/currencies/eur-brl-historical-data"),
    
~~~
---
## **TABELAS**

1. calendar

2. order_sale

3. order_billing

4. seller

5. customer

6. obt

7. Meses

8. general_target

9. Combustiveis

10. seller_target

11. Anos

12. Regionais

13. Marca

14. dim_return

15. LOGISTICA E CS

16. RLS_GERENTES

17. RLS_VENDEDORES

18. Feriados

19. Table

20. Table 2

21. USD

22. EUR

---
## **ATUALIZAÇÃO CONJUNTO DE DADOS**
Atualização diária do conjunto de dados, a cada 1 (uma) hora.

## **USABILIDADE**

---
## **ACESSO**


---

## **DOCUMENTAÇÃO POWER BI** <font size ="2"> - (clique abaixo para visualizar) </font>

[**Documentação**](AD_Corporativo/CORPORATIVO.htm)

[**Documentação_old**](AD_Corporativo/CORPORATIVO_old.pdf)