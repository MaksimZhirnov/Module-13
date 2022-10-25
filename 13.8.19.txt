price = 0
while True:
    try:
        ticket = input('Сколько билетов вы хотите приобрести на мероприятие? ')
        ticket = int(ticket)
        if type(ticket) == int:
            break
    except ValueError:
        print('Введите целое число')
for i in range(ticket):
    i = i+1
    while True:
        try:
            age = input(f'Введите возраст посетителя {i}? ')
            age = int(age)
            if age < 18:
                price = price+0
            elif 18 <= age < 25:
                price = price+990
            else:
                price = price+1390
            if type(age) == int:
                break
        except ValueError:
            print('Введите целое число')
if ticket > 3:
    price_all = price*0.9
    print(f' Итого сумма к оплате за {ticket} билета(ов) {price} руб. с учетом 10%-ой скидки за регистрацию более 3-х человек')
else:
    print(f'Итого сумма к оплате за {ticket} билета(ов) {price} руб.')