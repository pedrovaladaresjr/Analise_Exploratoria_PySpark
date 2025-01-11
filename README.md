# Análise Exploratória de Dados (EDA) com PySpark

## 1. Introdução
*`Este repositório está sendo atualizado à medida que o estudo vai avançando.`* 


- **Objetivo**: O objetivo deste projeto é entender como os `Dados do Bitcoin` tem se comportado nos últimos tempos e quais informações valiosas podemos tirar com isso.
  
- **Fonte dos dados**: utilização a biblioteca *yfinance* para extrair os dados histórios do Bitcoin de `2014-09-01` até a última atualização mais recente.
  
- **Ferramentas utilizadas**: PySpark, Python.
  

---

## 2. Carregamento dos Dados
Os dados foram carregados através de módulos do SparkSession.

```python
# Exemplo de código PySpark para carregar dados
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("Análise Exploratória").getOrCreate()

df = spark.read.csv("caminho/do/arquivo.csv", header = 'true', inferSchema= 'true')
