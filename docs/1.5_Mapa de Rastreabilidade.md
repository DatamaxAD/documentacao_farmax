# **Seja bem vindo (a)**

<font size ="2">
**Documentação dos dashboards do setor de <span style = "color: blue">Qualidade</span>, clique abaixo e navegue para o App no Power BI Service:**

<a href="https://app.powerbi.com/Redirect?action=OpenApp&appId=e88e92bc-c6dd-4cd4-b79e-2eb32b033931&ctid=4019cfa9-aae5-4964-912e-b0e0bb606d37" target="_blank">
**Aplicativo Qualidade**
</a>

---

<font size ="2">

## **OBJETIVO - RASTREABILIDADE**
É utilizado pelo Controle de Qualidade e Garantia da Qualidade para visualizar a data de validade, calcular a retirada dos produtos da retenção, e  rastrear o  consumo de materiais dentro da ordem de produção.

---

## **FONTE DE DADOS**

~~~
let
   Fonte = AmazonRedshift.Database("farmax-cluster.cdkgzqhbae0k.us-east-1.redshift.amazonaws.com","farmaxcluster"),
   qlt = Fonte{[Name="qlt"]}[Data],
   dim_traceability_materials1 = qlt{[Name="dim_traceability_materials"]}[Data]
~~~

---
## **TABELAS**

1. Rastreabilidade

2. Medidas

3. dCalendario	 

4. Parâmetro - Data	

5. Parâmetro - DT Vencimento		

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


### **VISÃO GERAL - DISTRIBUIÇÕES**

![Matriz](AD_Qualidade/RASTREABILIDADE_01_VISAO_GERAL.png)



**Glossário:**

1. Cards resumo numérico
2. Botão para limpar filtros
3. Visual: **Total de Materiais por Status** 
4. Visual: **Total de Materiais por Período de Vencimento**  <font size ="2"> - Ano / Trimestre / Mês / Dia / Dia da Semana  </font>
5. Visual: **Árvore Hierárquica - Insumos movimentados por utilização**
6. Visual: **Total de Lote PI - PA por Status**
7. Visual: **Total de Lote PI - PA  por Período de Vencimento**  <font size ="2"> - Ano / Trimestre / Mês / Dia / Dia da Semana  </font>
---


### **MATRIZ CONSULTIVA - RASTREABILIDADE**

![Matriz](AD_Qualidade/RASTREABILIDADE_02_MATRIZ.png)



**Glossário:**

1. Cards resumo numérico
2. Botão para limpar filtros
3. Filtro por **Data da Movimentação**
4. Filtro de Texto por **Descrição ou Código do Produto onde foi usado**
5. Filtro por **Código do Material utilizado**
6. Filtro por **Lote do Material utilizado**
7. Filtro de Texto por **Código do Produto onde foi usado**
8. Filtro Cliente por **Lote PI-PA**
---


## **DOCUMENTAÇÃO POWER BI** <font size ="2"> - (clique abaixo para visualizar) </font>


[**Documentação**](AD_Qualidade/DOC_PBI_RASTREABILIDADE.htm)

## **CANVAS** <font size ="2"> - (clique abaixo para visualizar) </font>

[**Canvas**](AD_Qualidade/CANVAS_QUALIDADE.pdf)

---

## **MANUAL DO USUÁRIO** <font size ="2"> - (clique abaixo para visualizar) </font>

[**Manual do Usuário**](AD_Qualidade/MANUAL_USUARIO.pdf)



</font>
