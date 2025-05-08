def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def factorial(n):
    if n < 0:
        return None
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result

def fibonacci(n):
    sequence = []
    a, b = 0, 1
    for _ in range(n):
        sequence.append(a)
        a, b = b, a + b
    return sequence

def sum_digits(n):
    return sum(int(d) for d in str(abs(n)))

def reverse_number(n):
    sign = -1 if n < 0 else 1
    return sign * int(str(abs(n))[::-1])

def main():
    while True:
        print("\n--- Numbers Toolkit ---")
        print("1. Check Prime")
        print("2. Factorial")
        print("3. Fibonacci Series")
        print("4. Sum of Digits")
        print("5. Reverse Number")
        print("6. Exit")
        choice = input("Choose an option: ")

        if choice == '1':
            num = int(input("Enter a number: "))
            print("Prime" if is_prime(num) else "Not Prime")
        elif choice == '2':
            num = int(input("Enter a number: "))
            print(f"Factorial: {factorial(num)}")
        elif choice == '3':
            count = int(input("How many terms? "))
            print(f"Fibonacci: {fibonacci(count)}")
        elif choice == '4':
            num = int(input("Enter a number: "))
            print(f"Sum of Digits: {sum_digits(num)}")
        elif choice == '5':
            num = int(input("Enter a number: "))
            print(f"Reversed: {reverse_number(num)}")
        elif choice == '6':
            print("Goodbye!")
            break
        else:
            print("Invalid option.")

if __name__ == "__main__":
    main()
