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
