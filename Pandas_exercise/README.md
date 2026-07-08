# Apuntes:

### 01_Getting_&_Knowing_Your_Data:

* **01_World Food Facts:**

`df.shape`: Filas y Columnas.

`df.dtypes['column_name']`: Nos da el *datatype* de la columna `column_name`.

* **02_Chipotle:**

`df['column_name'].count()`: Cuenta la cantidad de veces que aparece un elemento en la columna.

`df['column_name_num'].sum()`: Suma los valores numéricos de la columna indicada.

`df.groupby('column_name')`: Agrupa los valores de la columna indicada con el objetivo de poder aplicar funciones sobre los mismos.