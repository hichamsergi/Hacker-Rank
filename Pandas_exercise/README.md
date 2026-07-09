# Apuntes:

### 01_Getting_&_Knowing_Your_Data:

* **01_World Food Facts:**

`df.shape`: Filas y Columnas.

`df.dtypes['column_name']`: Nos da el *datatype* de la columna `column_name`.

* **02_Chipotle:**

`df['column_name'].count()`: Cuenta la cantidad de veces que aparece un elemento en la columna.

`df['column_name_num'].sum()`: Suma los valores numéricos de la columna indicada.

`df.groupby('column_name')`: Agrupa los valores de la columna indicada con el objetivo de poder aplicar funciones sobre los mismos.

`df[column_name].str.replace('$', '')`: Eliminar el carácter `$`, o substituirlo por lo que queramos.

`df[column_name].apply(lambda_function)`: Aplicamos una función lambda a una columna en concreto.

`df['column_name].nunique()`: Entendiendo el nombre de la función, *number of uniques*, podemos saber que se refiere a la cantidad de valores únicos de la columna indicada. 