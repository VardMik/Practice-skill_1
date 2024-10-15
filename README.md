# Practice-skill_1
first steps


# Task 1. Greeting.
#Condition. Write a program that asks the user for his name. In response to your input, a greeting should appear on the screen addressing the name entered earlier from the keyboard.

#Условие. Напишите программу, запрашивающую у пользователя его имя. В ответ на ввод на экране должно появиться приветствие с обращением по имени, введенному с клавиатуры ранее.

#We declare a variable with the ability to enter a username

#Объявляем переменную с возможность ввести имя пользователя
name = str(input('Введите ваше имя: '))

#Let's display a greeting with the username entered in the 'name' variable

#Вывподим на экран приветствие с именем пользователя, введеное в переменную 'name'
print('Привет!', name)


# Task 2. Souvenirs and trinkets.
#Condition. The online store sells various souvenirs and trinkets. Each souvenir weighs 75 g, and the trinket weighs 112 g. Write a program that asks the user for the number of both purchases, and then displays the total weight of the package.

#Условие. Интернет-магазин занимается продажей различных сувениров и безделушек. Каждый сувенир весит 75 г, а безделушка – 112 г. Напишите программу, запрашивающую у пользователя количество тех и других покупок, после чего выведите на экран общий вес посылки.

#We assign stock weight to souvenirs and trinkets

#Присваиваем стоковый вес сувениров и безделушек
suvenir = 75
bezdelushka = 112

#We ask the buyer for the number of souvenirs and trinkets in pcs. required for purchase

#Запрашиваем у покупателя количество сувениров и безделушек в шт. требуемых к покупке
suvenir_quantity = int(input('Введите желаемое количество сувениров в шт.: '))
bezdelushka_quantity = int(input('Введите желаемое количество безделушек в шт.: '))

#We calculate each product

#Производим расчет каждого из товаров

#Souvenirs #Сувениры
suvenir_all = suvenir * suvenir_quantity

#Buzz-trinkets #Бузделушки
bezdelushka_all = bezdelushka * bezdelushka_quantity

#We will calculate the total parcel 

#Произведем расчет общей посылки
weight_all = suvenir_all + bezdelushka_all

#Display the total weight of the parcel

#Выводим на экран общий вес посылки
print('Общий вес посылки составляет: ', weight_all)


# Problem 3. Compound interest
#Condition. Imagine that you opened a savings account at a bank at 4% per annum. The bank calculates interest at the end of the year and adds it to the invoice amount. Write a program that prompts the user for an initial deposit amount and then calculates and displays the amount in the account at the end of the first, second, and third years. All amounts must be rounded to two decimal places.

#Условие. Представьте, что вы открыли в банке сберегательный счет под 4 % годовых. Проценты банк рассчитывает в конце года и добавляет к сумме счета. Напишите программу, которая запрашивает у пользователя сумму первоначального депозита, после чего рассчитывает и выводит на экран сумму на счету в конце первого, второго и третьего годов. Все суммы должны быть округлены до двух знаков после запятой.

#Requesting an initial deposit on the account from the client

#Запрашиваем изначальный депозит по счету у клиента
a = int(input('Введите начальную сумму по сберегательному счету:'))

#We calculate the annual profit taking into account the annual rate of 4%

#Расчитываем ежегодную прибыдь с учетом годовой ставки 4% 

#Profit for 1 year and add to existing deposit

#Прибыль за 1 год и прибовляем к существующему депозиту
profit_1 = a + (a/100*4)

#Profit for the 2nd year and add the amount of the first year

#Прибыль за 2 год и прибовляем сумму первого года
profit_2 = profit_1 + (profit_1/100*4)

#Profit for the 3rd year and add the amount of the first year

#Прибыль за 3 год и прибовляем сумму первого года
profit_3 = profit_2 + (profit_2/100*4)

#Display the annual total with interest for the year

#Выводим на экран ежегодную итоговую сумму с процентами за год
print('Итоговая сумма по вкладу за 1 год составляет: ', '%.2f' % (profit_1))
print('Итоговая сумма по вкладу за 2 год составляет: ', '%.2f' % (profit_2))
print('Итоговая сумма по вкладу за 3 год составляет: ', '%.2f' % (profit_3))


# Problem 4. Arithmetic

#Condition. Create a program that prompts the user for two integers a and b and then displays the results of the following mathematical operations: 

#sum of a and b;

#difference between a and b;

#product of a and b;

#quotient of a divided by b;

#remainder of division of a by b;

#decimal logarithm of a;

#result of raising the number a to the power b.


#Условие. Создайте программу, которая запрашивает у пользователя два целых числа a и b, после чего выводит на экран результаты следующих математических операций: 
#сумма a и b;
#разница между a и b;
#произведение a и b;
#частное от деления a на b;
#остаток от деления a на b;
#десятичный логарифм числа a;
#результат возведения числа a в степень b.

#Since additional mathematical tools will be used, it is necessary to declare them

#Так как будут применяться дополнительные математические инструменты, необходиом их объявить
from math import log10

#Request the values ​​of a and b from the user

#Заправшиваем у пользователя значания a и b 
a = int(input('Введите значение первого целого числа: '))
b = int(input('Введите значение второго целого числа: '))
print('Сумма a и b =', a+b)
print('Разница между a и b =', a-b)
print('Произведение a и b =', a*b)
print('Частное от деления a на b = ', a/b)
print('Остаток от деления a на b = ', a%b)
print('Десятичный логарифм числа a = ', log10(a))
print('Результат возведения числа a в степень b = ', a**b)


# Problem 5. Exchange

#Condition. Imagine that you are writing software for an automatic cash register in a self-service store. One of the functions included in the cash register should be calculating change in case the customer pays in cash. Write a program that will ask the user for the amount of change in kopecks. After that, it should calculate and display on the screen how many and what kind of coins are needed to issue the specified amount, provided that the minimum possible number of coins should be used. Let's say we have coins of 1, 5, 10, 50 kopecks, as well as 1, 2 and 5 rubles.

#Условие. Представьте, что вы пишете программное обеспечение для автоматической кассы в магазине самообслуживания. Одной из функций, заложенных в кассу, должен быть расчет сдачи в случае оплаты покупателем наличными. Напишите программу, которая будет запрашивать у пользователя сумму сдачи в копейках. После этого она должна рассчитать и вывести на экран, сколько и каких монет потребуется для выдачи указанной суммы, при условии что должно быть задействовано минимально возможное количество монет. Допустим, у нас есть в распоряжении монеты достоинством в 1, 5, 10, 50 копеек, а также в 1, 2 и 5 рублей.

#We request the amount of change in kopecks from the user

#Запрашиваем количество сдачи в копейках у пользователя
kop_start = int(input('Введите количество сдачи в копейках: '))

#Indicate the stock values ​​of coins in denominations of 1, 5, 10, 50 kopecks, as well as 1, 2 and 5 rubles.

#Указываем стоковые значения монет достоинством в 1, 5, 10, 50 копеек, а также в 1, 2 и 5 рублей.
kop_1 = 1
kop_5 = 5
kop_10 = 10
kop_50 = 50
rub_1 = 100
rub_2 = 200
rub_5 = 500

#We calculate the number of required coins with denominations of 1, 5, 10, 50 kopecks, as well as 1, 2 and 5 rubles

#Расчитываем количество необходимых монет с номиналами в 1, 5, 10, 50 копеек, а также в 1, 2 и 5 рублей

#The number of coins with the nominal value of 5 rubles

#Количество монет номеналом 5 рублей
rub_5_quantity = kop_start / rub_5
kop = kop_start % rub_5

#The number of coins with the nominal value of 2 rubles

#Количество монет номеналом 2 рубля
rub_2_quantity = kop / rub_2
kop = kop % rub_2

#The number of coins with the denomination of 1 ruble

#Количество монет номеналом 1 рубль
rub_1_quantity = kop / rub_1
kop = kop % rub_1

#Number of coins with a nominal value of 50 kopecks

#Количество монет номеналом 50 копеек
kop_50_quantity = kop / kop_50
kop = kop % kop_50

#The number of coins with the nominal value of 10 kopecks

#Количество монет номеналом 10 копеек
kop_10_quantity = kop / kop_10
kop = kop % kop_10

#Number of coins with a nominal value of 5 kopecks

#Количество монет номеналом 5 копеек
kop_5_quantity = kop / kop_5
kop = kop % kop_5

#Number of coins with nominal value 1 kopeck

#Количество монет номеналом 1 копейка
kop_1_quantity = kop / kop_1
kop = kop % kop_1

#Calculate the amount in rubles

#Расчитаем сумму в рублях
all_rub = kop_start / 100

#Calculate the amount in kopecks

#Расчитаем сумму в копейках
all_kop = kop_start % 100

#Display the values ​​on the user's screen

#Выводим значения на экран пользователя
print("К оплате необходимо предоставить: ", int(all_rub), 'рублей', all_kop, "копейки")
print('Количество монет номеналом 5 рублей: ', int(rub_5_quantity))
print('Количество монет номеналом 2 рубля: ', int(rub_2_quantity))
print('Количество монет номеналом 1 рубль: ', int(rub_1_quantity))
print('Количество монет номеналом 50 копеек: ', int(kop_50_quantity))
print('Количество монет номеналом 10 копеек: ', int(kop_10_quantity))
print('Количество монет номеналом 5 копеек: ', int(kop_5_quantity))
print('Количество монет номеналом 1 копейка: ', int(kop_1_quantity))


# Problem 6. Yesterday's bread

#Condition. A bakery sells bread for 49 rubles per loaf. The discount on yesterday's bread is 60%. Write a program that will prompt the user for the number of yesterday's loaves of bread purchased. The output to the screen should include the regular price per loaf, the discounted price, and the total cost of the bread purchased. All values ​​should be output on separate lines with appropriate descriptions. Use a format with two decimal places and 5 character spaces for output.

#Условие. Пекарня продает хлеб по 49 рублей за буханку. Скидка на вчерашний хлеб составляет 60 %. Напишите программу, которая будет запрашивать у пользователя количество приобретенных вчерашних буханок хлеба. В вывод на экран должны быть включены обычная цена за буханку, цена со скидкой и общая стоимость приобретенного хлеба. Все значения должны быть выведены на отдельных строках с соответствующими описаниями. Используйте для вывода формат с двумя знаками после запятой и 5-ю знакоместами.

#We request the number of loaves to purchase from the consumer

#Запрашиваем количество буханок к покупке у потребителя
bread = int(input('Введите колличество буханок: '))

#Set the stock value of the loaf

#Задаем стоковое значение буханки
bread_stok = 49

#We calculate the price for 1 loaf taking into account the discount

#Расчитываем цену за 1 буханку с учетом скидки
bread_discount = bread_stok - (bread_stok/100*60)

#We calculate the total price for cash, taking into account the discount

#Расчитываем суммарную цену за хдеб с учетом скидки
bread_sum_discount = bread_discount * bread

#Display the values ​​on the user's screen

#Выводим значения на экран пользователя
print('%5s %.2f' % ("Обычная цена за 1 хлеб: ", bread_stok))
print('%5s %.2f' % ("Цена со скидкой за 1 хлеб: ", bread_discount))
print('%5s %.2f' % ("Общая стоимость пребретенного хлеба с учетом скидки, составляет: ", bread_sum_discount))
