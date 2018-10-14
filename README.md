# homework 4.1
a = ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "0", "14", "15"]

print("\n".join(map("|".join, zip(*[iter(a)]* 4)))) #zip(*[iter(s)]*n) - извлекает элемент из всех трех итераторов из списка по порядку. Поскольку все итераторы являются одним и тем же объектом, просто группирует список в кусках n.


b = ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14", "15", "0"]

while a != b:
    x = a.index(min(a))
    step = input ('Введите шаг: ')
    
    if step == 'left':
        d = a[x]
        a[x] = a[x-1]
        a[x-1] = d
        print("\n".join(map("|".join, zip(*[iter(a)]* 4))))
        if a == b:
            print ('You are a champion!')
            break
    
    elif step == 'right':
        d = a[x]
        a[x] = a[x+1]
        a[x+1] = d
        print("\n".join(map("|".join, zip(*[iter(a)]* 4))))
        if a == b:
            print ('You are a champion!')
            break
    
    elif step == 'up':
        d = a[x]
        a[x] = a[x-4]
        a[x-4] = d
        print("\n".join(map("|".join, zip(*[iter(a)]* 4))))
        if a == b:
            print ('You are a champion!')
            break
    
    elif step == 'down':
        d = a[x]
        a[x] = a[x+4]
        a[x+4] = d
        print("\n".join(map("|".join, zip(*[iter(a)]* 4))))
        if a == b:
            print ('You are a champion!')
            break
