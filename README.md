# homework-05-virt-01-basics

## Задача 1

Опишите кратко, как вы поняли: в чем основное отличие полной (аппаратной) виртуализации, паравиртуализации и виртуализации на основе ОС.

```
1. Аппаратная.
Гипервизор сам является ОС и имеет доступ к аппаратной чати напрямую.
2. Паравиртуализация.
Гипервизор через ОС хоста имеет доступ к аппаратным ресурсам.
3. Виртуализация уровня ОС.
Гипервизор - это изолированная ОС, но не может быть оличной от хостовой.
```

## Задача 2

Выберите один из вариантов использования организации физических серверов, в зависимости от условий использования.

Организация серверов:

физические сервера,
```
Высоконагруженная база данных, чувствительная к отказу. Большая стабильность работы.
Системы, выполняющие высокопроизводительные расчеты на GPU. Высокая производительность. 
```
паравиртуализация,
```
Windows системы для использования бухгалтерским отделом. Простота настройки. Доступность.
```

виртуализация уровня ОС.
```
Различные web-приложения. Каждое приложение в своем контейнере.
```

## Задача 3

Выберите подходящую систему управления виртуализацией для предложенного сценария. Детально опишите ваш выбор.
```
Можно вообще выбрать одно решение, на котором работает специалист и к которому привык.
Мне, напрмер, удобен VirtualBox.
```
Сценарии:

1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
```
vmWare. Высокопроизводительный. Встроенные программы бэкапа и балансировки.
```
2. Требуется наиболее производительное бесплатное open source решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
```
Я бы выбрал VirtulBox. Работает с разными дистрибутивами. Можно развернуть из ISO образа.
```
3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows инфраструктуры.
```
HyperV. Как продукт Microsoft
```
4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.
```
vagrant. Просто я его знаю и он для меня удобен. Можно настроить все в одном файле.
```

## Задача 4

Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, то создавали бы вы гетерогенную среду или нет? Мотивируйте ваш ответ примерами.
```
Гетерогенная среда приведет к увеличению расходов.(Инженеры, разное оборудование, несовместимость). Многие системы дублируют функционал друг друга.
Универсальная система посволит гибче производить настройки, упростит резервное копирование и переезд.
Все зависит от задач. Для моих текущих задач мне хватает Virtalbox.
```
