from random import randint


def attack(char_name, char_class, char_power):

    if char_class == 'warrior':
        caused_damage = char_power['атака'] + randint(3, 5)

        return (f'{char_name} нанёс урон противнику равный {caused_damage}')

    if char_class == 'mage':
        caused_damage = char_power['атака'] + randint(5, 10)

        return (f'{char_name} нанёс урон противнику равный {caused_damage}')

    if char_class == 'healer':
        caused_damage = char_power['атака'] + randint(-3, -1)

        return (f'{char_name} нанёс урон противнику равный {caused_damage}')


def defence(char_name, char_class, char_power):

    if char_class == 'warrior':
        blocked_defence = char_power['защита'] + randint(5, 10)

        return (f'{char_name} блокировал {blocked_defence} урона')

    if char_class == 'mage':
        blocked_defence = char_power['защита'] + randint(-2, 2)

        return (f'{char_name} блокировал {blocked_defence} урона')

    if char_class == 'healer':
        blocked_defence = char_power['защита'] + randint(2, 5)

        return (f'{char_name} блокировал {blocked_defence} урона')


def special(char_name, char_class, char_power):

    if char_class == 'warrior':
        applied_skill = char_power['выносливость'] + 25

        return (f'{char_name} применил специальное умение '
                f'«Выносливость {applied_skill}»')

    if char_class == 'mage':
        applied_skill = char_power['атака'] + 40

        return (f'{char_name} применил специальное умение '
                f'«Атака {applied_skill}»')

    if char_class == 'healer':
        applied_skill = char_power['защита'] + 30

        return (f'{char_name} применил специальное умение '
                f'«Защита {applied_skill}»')


def start_training(char_name, char_class, char_power):

    if char_class == 'warrior':
        print(f'{char_name}, ты Воитель — отличный боец ближнего боя.')

    if char_class == 'mage':
        print(f'{char_name}, ты Маг — превосходный укротитель стихий.')

    if char_class == 'healer':
        print(f'{char_name}, ты Лекарь — чародей, способный исцелять раны.')

    print('Потренируйся управлять своими навыками.')
    print('Введи одну из команд: attack — чтобы атаковать противника, '
          'defence — чтобы блокировать атаку противника или '
          'special — чтобы использовать свою суперсилу.')
    print('Если не хочешь тренироваться, введи команду skip.')

    cmd = None

    while cmd != 'skip':

        cmd = input('Введи команду: ')

        if cmd == 'attack':
            print(attack(char_name, char_class, char_power))

        if cmd == 'defence':
            print(defence(char_name, char_class, char_power))

        if cmd == 'special':
            print(special(char_name, char_class, char_power))

    return 'Тренировка окончена.'


def choice_char_class():

    approve_choice = None
    char_class = None

    while approve_choice != 'y':

        char_class = input('Введи название персонажа, '
                           'за которого хочешь играть:  '
                           'Воитель — warrior, '
                           'Маг — mage, '
                           'Лекарь — healer: ')

        if char_class == 'warrior':
            print('Воитель — дерзкий воин ближнего боя. '
                  'Сильный, выносливый и отважный.')

        if char_class == 'mage':
            print('Маг — находчивый воин дальнего боя. '
                  'Обладает высоким интеллектом.')

        if char_class == 'healer':
            print('Лекарь — могущественный заклинатель. '
                  'Черпает силы из природы, веры и духов.')

        approve_choice = input('Нажми (Y), чтобы подтвердить выбор, '
                               'или любую другую кнопку, '
                               'чтобы выбрать другого персонажа ').lower()

    return char_class


if __name__ == '__main__':

    char_power = {'выносливость':  80, 'атака': 5, 'защита': 10}

    print('Приветствую тебя, искатель приключений!')
    print('Прежде чем начать игру...')

    char_name = input('...назови себя: ')

    print(f'Здравствуй, {char_name}! Сейчас твоя '
          f'выносливость — {char_power["выносливость"]}, '
          f'атака — {char_power["атака"]} и '
          f'защита — {char_power["защита"]}.')
    print('Ты можешь выбрать один из трёх путей силы:')
    print('Воитель, Маг, Лекарь')

    char_class = choice_char_class()

    print(start_training(char_name, char_class, char_power))
