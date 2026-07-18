# Apuntes:

### 01_Getting_&_Knowing_Your_Data:

* **01_World Food Facts:**

`df.shape`: Filas y Columnas.

`df.dtypes['column_name']`: Nos da el *datatype* de la columna `column_name`.


* **02_Chipotle:**

`df['column_name'].count()`: Cuenta la cantidad de veces que aparece un elemento en la columna.

`df['column_name_num'].sum()`: Suma los valores numéricos de la columna indicada.

`df.groupby(['column_name'])`: Agrupa los valores de la columna indicada con el objetivo de poder aplicar funciones sobre los mismos.

`df[column_name].str.replace('$', '')`: Eliminar el carácter `$`, o substituirlo por lo que queramos.

`df[column_name].apply(lambda_function)`: Aplicamos una función lambda a una columna en concreto.

`df['column_name].nunique()`: Entendiendo el nombre de la función, *number of uniques*, podemos saber que se refiere a la cantidad de valores únicos de la columna indicada.


* **03_Occupation:**

`df['column_name'].value_counts()`: Cuenta la cantidad de veces que aparecen cada valor dentro de la columna.

`df.describe(include='all')`: Nos da información estadística de las columnas numéricas del DataFrame.


### 02_Filtering_&_Sorting:

* **01_Chipotle:**

`df['column_name'].astype(float)`: Transformamos el tipo de dato de una columna al indicado.

`df.loc[(...) & (...)]`: Para filtrar dadas 2 condiciones simultáneas.

`df.idxmax()`: Busca el índice del valor máximo.


* **02_Euro12:**

`df.sort_values(by=['column_1', 'column_2'])`: Ordena el DataFrame en función de las columnas que le indiquemos. El orden de las columnas es el orden que se seguirá.

`df.iloc[:, :]`: El **primer bloque** de dígitos corresponde a las **filas** que queremos obtener. El **segundo bloque** de dígitos corresponde a las **columnas** que queremos obtener.


* **03_Fictional_Army:**

`df.set_index('column', inplace=True)`: Indicando *inplace=True*, especificamos que modificamos el DataFrame original modificando el indice.

`df.loc[[...], [...]]`: Si establecemos un indice con datos string, el **primer bloque** corresponde a las **filas** que queremos obtener. El **segundo bloque** corresponde a las **columnas** que queremos obtener.


### 03_Grouping:

* **01_Regiment:**

`df.groupby('column', as_index=False)`: Con el argumento `as_index=False` lo que generamos es una salida sin estructura gerarquica, idea para generar un nuevo DataFrame.


* **02_Occupation:**

`df.groupby('column').is_X.mean()`: Obtenemos el porcentaje de valores no nulos respecto del total, muy util para obtener % de valores validos.

`df.groupby('column').age.agg(['min', 'max'])`: Para poder aplicar diferentes funciones a una columna, `agg` nos permite aplicarlas proporcionandolas como valores string(`agg(['min', 'max'])`).

`df.groupby(['column1', 'column2']).size()`: La función `size` cuenta la cantidad de registros que tiene la agrupación, dandonos por lo tanto un recuento. No es lo mismo que `count`, que si que diferencia con valores nulos(`NaN`).