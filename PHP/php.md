Нужные программы для прохождения <a style="text-decoration:none;" href="https://www.youtube.com/watch?v=Cwk4UqjR2JI&t=7s">курса</a> 
1. <a href="https://www.wampserver.com/ru/">Wamp server</a> или <a href="https://ospanel.io/download/">Open Server</a>
2. <a href="https://www.jetbrains.com/ru-ru/phpstorm/">PHP Storm</a>

<h2>Типы данных</h2>
<ul>
	<li>Integer/Float - <span>123, 55+23</span></li>
	<li>String - <span>'Привет'</span></li>
	<li>Boolean - <span>true, false</span></li>
	<li>Null - <span>null</span></li>
</ul>
<h2>Переменные</h2>
```
<?php  
  
$name = 'Artem';  
$age = '20';  
$hobby = 'swiming';  
$isMarried = 'false';  - прописывать булевые значение нужно верблюжей нотацией
echo $name;  
echo $age;  
echo $hobby;
```

echo $name  . "\n"; - код переноса строки 

```
. "\n"
```

<h2>Массивы</h2>
```
<?php  
  
$person = ['Artem', 20, 'swiming', true];  
    
print_r ($person);
```
 Этот вид кода, нужен для вывода массива, который нам нужен
 
 Результат запроса
```
(
    [0] => Artem
    [1] => 20
    [2] => swiming
    [3] => 1
)
```


Также в массиве можно прописывать ключ самому

```
<?php  
  
$person = ['name' => 'Artem', 20, 'swiming', true];  
  
$name = 'Artem';  
$age = 20;  
$hobby = 'swiming';  
$isMarried = true;  
  
print_r ($person);
```

Результат запроса
```
(
    [name] => Artem
    [0] => 20
    [1] => swiming
    [2] => 1
)

```
<p style='color: red;'>ключ и значение</p>
^ ассоциация к массиву

```
$person = [  
    'name' => 'Artem',  
    'age' => 20,  
    'hobby' => 'swiming',  
    'is_married' => true  
];

print_r ($person);
```


Результат запроса

```
(
    [name] => Artem
    [age] => 20
    [hobby] => swiming
    [is_married] => 1
)
```


Для вызова конкретного ключа, прописываем - print_r ($person['name']);


<h2>Многомерные массивы</h2>
Пример кода

```
$persons = [  
    [  
        'name' => 'Artem',  
        'age' => 20,  
        'hobby' => 'swiming',  
        'is_married' => true  
    ],  
    [  
        'name' => 'Anton',  
        'age' => 22,  
        'hobby' => 'fishing',  
        'is_married' => false  
    ],  
    [  
        'name' => 'Alena',  
        'age' => 21,  
        'hobby' => 'dance',  
        'is_married' => true  
    ]  
  
];
```

Результат запроса

```
print_r ($persons);

Array
(
    [0] => Array
        (
            [name] => Artem
            [age] => 20
            [hobby] => swiming
            [is_married] => 1
        )
    [1] => Array
        (
            [name] => Anton
            [age] => 22
            [hobby] => fishing
            [is_married] => 
        )
    [2] => Array
        (
            [name] => Alena
            [age] => 21
            [hobby] => dance
            [is_married] => 1
        )
)
```

