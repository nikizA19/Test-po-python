# Test-po-python


Bate dano da  ne trqq da hodq na izpit
 Izchislqvane na lihvata za sledvashtiq mesec 
 
def calculate_monthly_interest(): 
    balance = float(input("Въведете текущия баланс: "))
    annual_interest_rate = float(input("Въведете годишния лихвен процент (в %): "))
    interest = balance * (annual_interest_rate / 1200)
    print(f"Лихвата за следващия месец е: {interest:.2f} валутни единици")

if __name__ == "__main__":
    calculate_monthly_interest()


Tri modula ot math 
   import math

def apply_math_functions():
    number = float(input("Въведете число: "))
    sqrt_result = math.sqrt(number) if number >= 0 else "Невалидно (отрицателно число)"
    sin_result = math.sin(number)
    log_result = math.log(number) if number > 0 else "Невалидно (неположително число)"   
    print(f"Квадратен корен: {sqrt_result}")
    print(f"Синус: {sin_result:.2f}")
    print(f"Логаритъм (натурален): {log_result}")

if __name__ == "__main__":
    apply_math_functions()

Visokosna godina
def is_leap_year(year):
    # Проверка дали годината е високосна
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return True
    return False

def main():
    try:
        # Въвеждане на година от потребителя
        year = int(input("Въведете година: "))
        if year <= 0:
            print("Грешка: Годината трябва да бъде положително число.")
        else:
            # Проверка дали годината е високосна
            if is_leap_year(year):
                print(f"{year} е високосна година.")
            else:
                print(f"{year} не е високосна година.")
    except ValueError:
        print("Грешка: Моля, въведете валидно цяло число за година.")

if __name__ == "__main__":
    main()

Smqta nadnicata za sedmica ako ima i overtime 
def calculate_weekly_salary():
    try:
        # Въвеждане на отработените часове и почасовата ставка
        hours_worked = float(input("Въведете броя на отработените часове: "))
        hourly_rate = float(input("Въведете почасовата ставка: "))
        # Проверка за извънредни часове
        if hours_worked > 40:
            regular_hours = 40
            overtime_hours = hours_worked - 40
            overtime_rate = hourly_rate * 1.5
            total_salary = (regular_hours * hourly_rate) + (overtime_hours * overtime_rate)
        else:
            total_salary = hours_worked * hourly_rate
        # Резултат
        print(f"Седмичната заплата е: {total_salary:.2f} валутни единици")
    except ValueError:
        print("Грешка: Моля, въведете валидни числови стойности.")

if __name__ == "__main__":
    calculate_weekly_salary()   




   Counting number and gives avg -------
    def process_numbers():
    print("Въведете цели числа (въведете 0, за да приключите):")
    positive_count = 0
    negative_count = 0
    total_sum = 0
    count = 0
    while True:
        try:
            number = int(input("Въведете число: "))  
            if number == 0:
                break  # Прекратяване на цикъла, ако е въведено 0          
            if number > 0:
                positive_count += 1
            elif number < 0:
                negative_count += 1  
            total_sum += number
            count += 1
        except ValueError:
            print("Грешка: Моля, въведете валидно цяло число.")
    if count > 0:
        average = total_sum / count
        print(f"Брой положителни числа: {positive_count}")
        print(f"Брой отрицателни числа: {negative_count}")
        print(f"Обща стойност: {total_sum}")
        print(f"Средна стойност: {average:.2f}")
    else:
        print("Не са въведени валидни числа.")

if __name__ == "__main__":
    process_numbers()
--------------------------------
-    def find_top_two_scores():
    try:
        # Въвеждане на броя на учениците
        num_students = int(input("Въведете броя на учениците: "))
        
        if num_students < 2:
            print("Грешка: Трябва да има поне двама ученици.")
            return

        # Списъци за съхранение на имената и резултатите
        students = []

        # Въвеждане на данни за всеки ученик
        for _ in range(num_students):
            name = input("Въведете името на ученика: ")
            score = float(input(f"Въведете резултата на {name}: "))
            students.append((name, score))

        # Сортиране на учениците по резултатите в низходящ ред
        students.sort(key=lambda x: x[1], reverse=True)

        # Показване на двата най-високи резултата
        print(f"Най-висок резултат: {students[0][0]} с резултат {students[0][1]:.2f}")
        print(f"Втори най-висок резултат: {students[1][0]} с резултат {students[1][1]:.2f}")
    except ValueError:
        print("Грешка: Моля, въведете валидни числови стойности за резултатите.")
    except IndexError:
        print("Грешка: Няма достатъчно ученици за сравнение.")

if __name__ == "__main__":
    find_top_two_scores()


Proverqvane dali e palindrome 

def is_palindrome():
    # Въвеждане на дума от потребителя
    word = input("Въведете дума: ").strip()
    # Проверка дали думата е палиндром
    if word == word[::-1]:
        print(f"'{word}' е палиндром.")
    else:
        print(f"'{word}' не е палиндром.")

if __name__ == "__main__":
    is_palindrome()


Proverqva kolko glavni i kolko malki bukvi ima v izraza 
    def count_letters(expression):
    # Инициализиране на броячи
    uppercase_count = 0
    lowercase_count = 0
    # Преброяване на главните и малките букви
    for char in expression:
        if char.isupper():
            uppercase_count += 1
        elif char.islower():
            lowercase_count += 1
    return uppercase_count, lowercase_count

# Пример за използване
if __name__ == "__main__":
    expression = input("Въведете израз: ")
    uppercase, lowercase = count_letters(expression)
    print(f"Главни букви: {uppercase}, Малки букви: {lowercase}")
