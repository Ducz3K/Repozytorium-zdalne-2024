Łukasz Dudicz
Dokumentacja do aplikacji
def add(x, y):
    """Dodawanie"""
    # Funkcja dodaje dwie liczby i zwraca wynik
    return x + y

def subtract(x, y):
    """Odejmowanie"""
    # Funkcja odejmuje drugą liczbę od pierwszej i zwraca wynik
    return x - y

def multiply(x, y):
    """Mnożenie"""
    # Funkcja mnoży dwie liczby i zwraca wynik
    return x * y

def divide(x, y):
    """Dzielenie"""
    # Funkcja dzieli pierwszą liczbę przez drugą
    # Sprawdza, czy druga liczba nie jest zerem, aby uniknąć dzielenia przez zero
    if y == 0:
        return "Błąd! Dzielenie przez zero."
    return x / y

def calculator():
    # Wyświetlenie powitalnej wiadomości
    print("Witaj w kalkulatorze!")
    # Wyświetlenie dostępnych operacji
    print("Wybierz operację:")
    print("1. Dodawanie")
    print("2. Odejmowanie")
    print("3. Mnożenie")
    print("4. Dzielenie")

  while True:
        # Poproszenie użytkownika o wybór operacji
        choice = input("Wprowadź numer operacji (1/2/3/4): ")

  # Sprawdzenie, czy wybór jest poprawny (1, 2, 3 lub 4)
  if choice in ('1', '2', '3', '4'):
            # Poproszenie użytkownika o wprowadzenie dwóch liczb
            num1 = float(input("Wprowadź pierwszą liczbę: "))
            num2 = float(input("Wprowadź drugą liczbę: "))

   # Wykonanie odpowiedniej operacji na podstawie wyboru użytkownika
  if choice == '1':
                print(f"Wynik: {num1} + {num2} = {add(num1, num2)}")

   elif choice == '2':
                print(f"Wynik: {num1} - {num2} = {subtract(num1, num2)}")

   elif choice == '3':
                print(f"Wynik: {num1} * {num2} = {multiply(num1, num2)}")

  elif choice == '4':
                # Dla dzielenia, funkcja divide zwróci komunikat, jeśli użytkownik spróbuje podzielić przez zero
                result = divide(num1, num2)
                print(f"Wynik: {num1} / {num2} = {result}")

  # Zapytanie użytkownika, czy chce wykonać kolejne obliczenie
  next_calculation = input("Czy chcesz wykonać kolejne obliczenie? (tak/nie): ")
   # Jeśli użytkownik nie chce kontynuować, przerwij pętlę
  if next_calculation.lower() != 'tak':
                break
        else:
  # Jeśli wybór nie jest prawidłowy, poinformuj użytkownika i pozwól mu spróbować ponownie
   print("Nieprawidłowy wybór. Spróbuj ponownie.")

# Uruchomienie funkcji calculator tylko jeśli skrypt jest uruchamiany bezpośrednio, a nie importowany jako moduł
if __name__ == "__main__":
    calculator()
