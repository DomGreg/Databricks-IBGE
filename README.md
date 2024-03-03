## Injestão de dados com Databricks através da API do IBGE
###### Devido as limitações do Databricks Community, não foi possível fazer integração com o Git, por isso o código foi printado. 

#### O código realiza uma requisição HTTP, processa os dados da resposta usando PySpark, renomeia algumas colunas do DataFrame resultante e, se a requisição for bem-sucedida, imprime informações sobre o DataFrame; caso contrário, imprime uma mensagem de falha.

![IBGE-1](https://github.com/DomGreg/Databricks-IBGE/assets/33266454/a49c89a5-b3fb-4044-a0d1-c6abe72059e9)
<br>

##### Dados Brutos em formato Json
![IBGE-2](https://github.com/DomGreg/Databricks-IBGE/assets/33266454/d76c041c-8ae5-42b6-8d53-0e143d072ad6)
<br>

##### O código está realizando uma operação de "explod" uma coluna que contém uma estrutura complexa (array) em linhas individuais, seguida por uma operação de pivotamento para transformar essas linhas em colunas usando as chaves do mapa original. O resultado é um novo DataFrame onde as informações estão organizadas de forma diferente em relação ao DataFrame original.
![IBGE-3](https://github.com/DomGreg/Databricks-IBGE/assets/33266454/3bee9a61-3756-44a3-b2e8-436d16a6f4c1)
<br>

##### Esse código trata valores nulos em colunas específicas do DataFrame df_spark_novo substituindo-os pelo valor padrão "Não informado". Isso é útil para lidar com dados ausentes e garantir que o DataFrame não contenha valores nulos nessas colunas específicas.
![IBGE-4](https://github.com/DomGreg/Databricks-IBGE/assets/33266454/8464573f-b2e4-4832-8d63-e0b1e8deca46)
<br>

#### Esse trecho de código resultará na gravação do DataFrame df_spark_novo em arquivos CSV no diretório especificado, onde cada partição do DataFrame será escrita como um arquivo CSV separado. As colunas serão separadas por vírgulas e a primeira linha do arquivo conterá os nomes das colunas, graças ao parâmetro header=True.
![IBGE-5](https://github.com/DomGreg/Databricks-IBGE/assets/33266454/137cce05-a99a-4bd0-946e-d83429b8298d)
<br><br><br>
### O código apresenta uma série de operações utilizando o PySpark, uma biblioteca do ecossistema Apache Spark.

### Manipulação eficiente de grandes conjuntos de dados com o PySpark;

### Exploração e transformação flexíveis de dados: As operações realizadas no código, como explodir uma coluna, pivotar dados, substituir valores nulos e renomear colunas, são transformações comuns em análise de dados;

### Paralelismo e processamento distribuído;

### Tratamento de dados ausentes: Substituir valores nulos por um valor padrão pode ser crucial para evitar problemas durante análises subsequentes ou ao alimentar algoritmos de aprendizado de máquina, garantindo que não haja lacunas nos dados;

### Exportação de dados para CSV: O código finaliza com a exportação dos dados processados para arquivos CSV locais. Isso pode ser útil para compartilhar os resultados ou integrar esses dados transformados em outros sistemas;
<br><br><br><br>
## Desenvolvedores/Contribuintes :octocat:

<p align="center">
<img src="https://user-images.githubusercontent.com/33266454/172633100-74def689-d7a1-40b6-8378-6f2567ba1941.png" height=400px width=400px>
</p>
<p align="center">
Gregório Silva
</p>
<br><br>
</p>







