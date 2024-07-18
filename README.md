# Atlantico-Avanti-Atividade-2
Tema: Algoritmos básicos de programação em linguagem python e visualização e análise de dados

## 1. Escreva uma função que receba uma lista de números e retorne outra lista com os números ímpares.

```
def odd_numbers(numbers):
    return [number for number in numbers if number % 2 != 0]
    
numbers = [7, 2, 5, 0, 1, 4, 8, 10]
print(odd_numbers(numbers))

# Output: [7, 5, 1]
```

## 2. Escreva uma função que receba uma lista de números e retorne outra lista com os números primos presentes.

```
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True

numbers = [7, 2, 5, 0, 1, 4, 8, 10]
primes = [number for number in numbers if is_prime(number)]
print(primes)

# Output: [7, 2, 5]
```

## 3. Escreva uma função que receba duas listas e retorne outra lista com os elementos que estão presentes em apenas uma das listas.

```
def unique_elements(list1, list2):
    result = []

    for item in list1:
        if item not in list2:
            result.append(item)

    for item in list2:
        if item not in list1:
            result.append(item)

    return result

list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]

print(unique_elements(list1, list2))

# Output: [1, 2, 3, 6, 7, 8]

```

## 4. Dada uma lista de números inteiros, escreva uma função para encontrar o segundo maior valor na lista.

```
def second(list_num):
    ordered_list = sorted(list_num, reverse=True)
    max_num = ordered_list[0]
    
    for i in ordered_list[1:]:
        if i < max_num:
            return i

    return None

numbers = [10, 5, 2, 0, 7, 10, 1]
print(second(numbers))

# Output: 7
```

## 5. Crie uma função que receba uma lista de tuplas, cada uma contendo o nome e a idade de uma pessoa, e retorne a lista ordenada pelo nome das pessoas em ordem alfabética.
```
def sort_by_name(people):
    sorted_people = sorted(people, key=lambda person: person[0])
    return sorted_people

people = [("Talita Dias", 24), ("Jéssica Vitória", 21), ("João Silva", 19), ("Dave", 20)]
sorted_people = sort_by_name(people)
print(sorted_people)

# Output: [('Dave', 20), ('João Silva', 19), ('Jéssica Vitória', 21), ('Talita Dias', 24)]
```

## 6. Observe os espaços sublinhados e complete o código.

```
import matplotlib.pyplot as plt
import numpy as np

fig, axs = plt.subplots(ncols=2, nrows=2, figsize=(5.5, 3.5), layout="constrained")
    for row in range(2):
        for col in range(2):
            axs[row, col].annotate(f'axs[{row}, {col}]', (0.5, 0.5),
                transform=axs[row, col].transAxes,
                ha='center', va='center', fontsize=18,
                color='darkgrey')
fig.suptitle('plt.subplots()')
```

## 7. Observe os espaços sublinhados e complete o código.

```
import numpy as np
import matplotlib as mpl
import matplotlib.pylot as plt

x = np.linspace(-2 * np.pi, 2 * np.pi, 100)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y)
```

## 8. Utilizando pandas, como realizar a leitura de um arquivo CSV em um DataFrame e exibir as primeiras linhas?

```
import pandas as pd
df = pd.read_csv('arquivo.csv')
df.head()
```

## 9. Utilizando pandas, como selecionar uma coluna específica e filtrar linhas em um “DataFrame” com base em uma condição?

```
df[df['estado'] == 'Amazonas']
```

## 10.Utilizando pandas, como lidar com valores ausentes (NaN) em um DataFrame?

Para lidar com valores ausentes (NaN) em um DataFrame utilizando pandas, podemos usar várias abordagens dependendo do que se deseja fazer com esses valores.

Exemplo:
```
import pandas as pd

# Read the CSV file into a DataFrame
df = pd.read_csv('file_name.csv')

# Check for missing values
print("Missing values by column:")
print(df.isna().sum())

# Remove rows with missing values
df_without_nan = df.dropna()

# Fill missing values with the mean of the columns
df_filled = df.fillna(df.mean())

# Display the DataFrame without missing values
print("DataFrame without missing values (rows removed):")
print(df_without_nan)

# Display the DataFrame with missing values filled
print("DataFrame with missing values filled:")
print(df_filled)

```
