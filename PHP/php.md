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

```
foreach ($person as $key) => {
	echo $key . ':';
	echo $item . "\n";
}
конструкция для перебора массива
```

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

Выведем массивы через цикл

Пример кода
```
$persons = [  
    [  
        'name' => 'Artem',  
        'age' => 20,  
        'hobby' => 'swiming',  
        'is_married' => true,  
        'cars' => ['mers', 'volga', 'moskvich']  
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
Array
(
    [name] => Artem
    [age] => 20
    [hobby] => swiming
    [is_married] => 1
    [cars] => Array
        (
            [0] => mers
            [1] => volga
            [2] => moskvich
        )

)
1Array
(
    [name] => Anton
    [age] => 22
    [hobby] => fishing
    [is_married] => 
)
1Array
(
    [name] => Alena
    [age] => 21
    [hobby] => dance
    [is_married] => 1
)
1
```

Чтобы получить имена, нужно прописать следующее

foreach ($persons as $person) {  
    echo print_r($person['name']);  
}
<span style='color: f1f1f1; text-decoration: underline;'>foreach</span> - цикличный оператор
Результат запроса

Artem1Anton1Alena1

<h2>Условный оператор</h2>
<span style="font-size: 30px;">if</span> - реализует выполнение определённых команд при условии, что некоторое логическое выражение (условие) принимает значение «истина» true.

```
$name = 'Anton';  
  
if ($name){  
    echo 'Yes';  
}
```

В скобках идёт конвертирование в true или false
И если конвертация превращается в true, результат выходит и выводится echo.

Если в переменной стоит null, то ошибки не будет, но интерпретатор будет определять как пустота. 

Если интерпретатор видит число или ноль, получаем то, что заходит, это и есть условный оператор.

<span style="font-size: 30px;">else</span> - с инициализатором и **операторами** if-constexpr для управления **условным** ветвлением.

```
$name = null;  
  
if ($name){  
    echo 'Yes';  
} else {  
    echo 'No';  
}
```

При такой варианте, можно отслеживать, что в переменной

Для перебора массива и просмотра нужного ключа, нужно прописать условие

```
if ($persons[2]['is_married']) {  
    echo 'is_married=true';  
} else{  
    echo 'is_married=false';  
}


Также через foreach

foreach ($persons as $person) {  
    echo ($person['is_married']);  
}

Результат 11


Или с выводом индекса массива

foreach ($persons as $index => $person) {  
    echo "Index: $index, is_married: " . ($person['is_married'] ? 'true' : 'false') . "\n";  
}

Результат

Index: 0, is_married: true
Index: 1, is_married: false
Index: 2, is_married: true


```
$persons[2] - число массива в массиве

<h2>Операторы сравнения</h2>

<span style="font-size: 30px;">==</span> - присваивание
<span style="font-size: 30px;">===</span> - строгое сравнение
<span style="font-size: 30px;">&&</span> - оператор И
<span style="font-size: 30px;">||</span> - оператор или


```
$name = 'Gena';  
$age = 10;  
  
if ($name=='Gena' && $age == 20){  
    echo 'Yes';  
} else {  
    echo 'No';  
}

Результат будет No

Если один из операторов не проходит значение, то результат отрицателен false
Если стоит оператор || то при выполнении одного из условий, результат true
```

продолжить с 9го урока