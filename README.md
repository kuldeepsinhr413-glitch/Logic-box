# Logic-box
def main():
    print("=== Shape Drawer ===")
    print("1. Square")
    print("2. Rectangle")
    print("3. Triangle")
    print("4. Number Analyzer")

    choice = input("Enter your choice: ")

    if choice == "1":
        rows = int(input("Enter number of rows: "))
        for _ in range(rows):
            print("* " * rows)

    elif choice == "2":
        rows = int(input("Enter number of rows: "))
        cols = int(input("Enter number of columns: "))
        for _ in range(rows):
            print("* " * cols)

    elif choice == "3":
        height = int(input("Enter height of triangle: "))
        for i in range(1, height + 1):
            print("* " * i)

    elif choice == "4":
        number_analyzer()

    else:
        print("Invalid choice. Please try again.")


def number_analyzer():
    print("\n=== Number Analyzer ===")
    numbers = []

    n = int(input("How many numbers do you want to enter? "))
    for i in range(n):
        num = int(input(f"Enter number {i+1}: "))
        numbers.append(num)

    print("\nResults:")
    print(f"Numbers: {numbers}")
    print(f"Maximum: {max(numbers)}")
    print(f"Minimum: {min(numbers)}")
    print(f"Sum: {sum(numbers)}")
    print(f"Average: {sum(numbers)/len(numbers):.2f}")


# Run the program
main()
