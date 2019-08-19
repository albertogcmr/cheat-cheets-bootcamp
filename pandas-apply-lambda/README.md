# Pandas Apply Lambdas

## Oficial documentation
[link](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html)

```python
>>> df = pd.DataFrame([[4, 9]] * 3, columns=['A', 'B'])
>>> df
   A  B
0  4  9
1  4  9
2  4  9
```

```python
>>> df.apply(np.sqrt)
     A    B
0  2.0  3.0
1  2.0  3.0
2  2.0  3.0
```

```python
>>> df.apply(np.sum, axis=0)
A    12
B    27
dtype: int64
```

```python
>>> df.apply(np.sum, axis=1)
0    13
1    13
2    13
dtype: int64
```

## Basic apply

Añade 3 a todos los elementos de la columna 'column'. 

```python
def add_3(a): 
    return a + 3

df['new_column'] = df['column'].apply(add_3, axis=1)
```

## Advanced apply

1. Crea una nueva columna combinación de dos columnas. 

```python
def combine(a, b): 
    if b: 
        return '{}-{}'.format(a, b)
    else: 
        return a

df_pokemon['combo'] = df_pokemon.apply(lambda x: combine(x['Type 2'], x['Type 2']), axis=1)
```

2. Crea dos columnas a partir de una. 

```python
def two_outputs(a): 
    return [a+3, a+6]
    
df['add_3'], df['add_6'] = zip(*df['A'].map(two_outputs))
```