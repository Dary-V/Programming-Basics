# Принципы и понятия ООП, а также принципы SOLID #

Рассмотрим основные понятия и принципы ООП на примере класса млекопитающих

В качестве римера берем:
* Лошадь
* Осел
* Корова

# Класс #

В данном случае ласс млекопитающие содержит подробное описание животных, в него входящих, например:

* Живородящие
* Теплокровные
* Имеющие волосяной покров, закрывающий все тело или его часть
* Кормящие молоком потомство

Все три объекта содержат признаки этого класса

# Объект #

В данном случае объектом является представитель класса, обладающий (в применении к коровам, лошадям и ослам нельзя сказать
сделанный по заданны параметрам класса) основными параметрами (признаками) класса:
корова, лошадь и осел - живородящие, теплокровные, имеют волосяной покров, вскармливают потомство молоком.

# Наследственность #

Все три предстаителя общего класса млекопитающие (корова, лошадь, осел) наследовали общие черты всего класса. Но, в
зависимости от конечной специализации, имеют в цепочке наследования свои подклассы, а также обладают уникальными
особенностями (можно сказать, например, что корова имеет ряд переопределеных особенностей для большей специализации)

# Полиморфизм #

Лошадь и осел в большей степени являются полиморфными так как могут с разными типами задач внутри одной функции - перевозка
людей\груза. Например - лошадь может перевозить одного человека верхом, одного человека на телеге, несколько людей,
перевозить груз. ДЛя этого не требуется модификация самой лошади, достаточно добавить ей дополнительный модуль (седло, телега).

# Инкапсуляция #

Все три объекта являются закрытыми, их невозможно модифицировать, внеся изменения в них непосредственно,
только через наследственность.

# Абстракции #

В случае с лошадью, ослом и коровой - для выполения ими необходимых функций абсолютно не нужно подробно знать их внутреннее
устройство. Достаточно представить их  виде абстракции (например лошадь - тянуть поводья лево\право\на себя, дополнительный
инструмент хлыст для увеличения скорости).

# Принципы SOLID #

1. Принцип единственной обязанности\ответственности - все три объекта имеют узкую специализацию. Лошадь и осел - перевозка
   груза, тягловая работа. Корова - производство продуктов питания
2. Принцип открытости\закрытости - и корова, и осел, и лошадь закрыты для модификации (невозможно изменить вмешательством
   их внутреннее устройство), но открыты для расширения ( например, можно, добавив к лошади плуг, расширить ее возможности)
3. Принцип подстановки Барбары Лисков - есть необходимая функция "перевозка" и производные от нее - перевозка грузов, перевозка людей.
   Лошадь и осел вполне соответствуют этому принципу.
4. Принцип разделения интерфейса - лошадь, осел и корова имеют отдельные интерфейсы для управления (глаза, уши, дополнительный
   интерфейс в виде упряжи), кормления, удаления отходов жизнедеятельности.
5. Принцип инверсии зависимостей. Если представить себе что лошадь - модуль верхнего уровня, а телега - модуль нижнего - то
   телега зависит от лошади, поскольку принцип устройства телеги должен быть согласован с лошадью (например, будет
   проблематично прицепить на телегу три колеса вместо двух или четырех). И  при этом и лошадь и телега зависят от абстракций
   (например от елементов управления).