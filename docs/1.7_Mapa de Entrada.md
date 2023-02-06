# **Seja bem vindo (a)**

<font size ="2">
**Documentação dos dashboards do setor de <span style = "color: blue">Qualidade</span>, clique abaixo e navegue para o App no Power BI Service:**

<a href="https://app.powerbi.com/Redirect?action=OpenApp&appId=e88e92bc-c6dd-4cd4-b79e-2eb32b033931&ctid=4019cfa9-aae5-4964-912e-b0e0bb606d37" target="_blank">
**Aplicativo Qualidade**
</a>

---

<font size ="2">

## **OBJETIVO - DEVOLUÇÕES**
É utilizado para rastreabilidade de materiais comprados.

---

## **FONTE DE DADOS**

~~~
let
    Fonte = AmazonRedshift.Database("farmax-cluster.cdkgzqhbae0k.us-east-1.redshift.amazonaws.com","farmaxcluster"),
    qlt = Fonte{[Name="qlt"]}[Data],
    dim_product_input_map1 = qlt{[Name="dim_product_input_map"]}[Data]
~~~

---
## **TABELAS**

1. Mapa de Entrada

2. Medidas

3. dCalendario	 

4. Parâmetro - TOP N

5. Parâmetro - DT VALIDADE		

6. Última Atualização	
	

---
## **ATUALIZAÇÃO CONJUNTO DE DADOS**
Atualização diária do conjunto de dados, às 06:30 / 08:30 / 10:30 / 12:30 / 14:30 / 16:30 / 18:30.

---
## **ACESSO**
Acesso via aplicativo Power BI, da seguinte forma:

<a href="https://app.powerbi.com/home" target="_blank">

1. Acessar **powerbi.com.br** </a>

2. Ir no painel de Navegação, opção "Aplicativos" ou "Aplicações"

3. Clicar no Aplicativo - Imagem abaixo>

![Imagem App Mkt](AD_Qualidade/APP_QUALIDADE.png)

---

## **USABILIDADE**


### **VISÃO GERAL - DEVOLUÇÕES**

![Matriz](AD_Qualidade/ENTRADAS_01_VISAO_GERAL.png)



**Glossário:**

1. Cards resumo numérico
2. Botão para limpar filtros
3. Filtro: **por Data de Lançamento**
4. Filtro: **por Data de Vencimento**
5. Filtro: **por Forcecedor**
6. Filtro: **por Material**
7. Visual:**Total de Materiais por Status de Vencimento**  <font size ="2"> - Ano / Trimestre / Mês / Dia / Dia da Semana  </font>
8. Visual:**Total de Materiais por Período de Validade**  <font size ="2"> - Ano / Trimestre / Mês / Dia / Dia da Semana  </font>
9. Visual: **Top Materiais por Total de Entradas**
10. Visual: **Top Fornecedores por Total de Entradas**

---

### **MATRIZ CONSULTIVA - RASTREABILIDADE**

![Matriz](AD_Qualidade/ENTRADAS_02_MATRIZ.png)



**Glossário:**

1. Cards resumo numérico
2. Botão para limpar filtros
3. Filtro por **Data de Lançamento**
4. Filtro de Texto por **Descrição, Código, Lote  ou NF do Produto**
5. Filtro por **Código do Material**
6. Filtro por **Descrição do Material**
7. Filtro por **Lote**
8. Filtro por **NF**
---


## **DOCUMENTAÇÃO POWER BI** <font size ="2"> - (clique abaixo para visualizar) </font>


[**Documentação**](AD_Qualidade/DOC_PBI_ENTRADAS.htm)

## **CANVAS** <font size ="2"> - (clique abaixo para visualizar) </font>

[**Canvas**](AD_Qualidade/CANVAS_QUALIDADE.pdf)

---

## **MANUAL DO USUÁRIO** <font size ="2"> - (clique abaixo para visualizar) </font>

[**Manual do Usuário**](AD_Qualidade/MANUAL_USUARIO.pdf)



</font>
