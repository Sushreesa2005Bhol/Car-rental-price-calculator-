# Car-rental-price-calculator-

cars = {
    "Hatchback": 1500,
    "Sedan": 2500,
    "SUV": 3500
}

def calculate_rent():
    print("Available cars:")

    for car, price in cars.items():
        print(car, "- Rs.", price, "per day")

    car_type = input("Enter car type: ").title()

    if car_type not in cars:
        print("Invalid car type!")
        return

    days = int(input("Enter number of days: "))

    if days <= 0:
        print("Days must be positive!")
        return

    total = cars[car_type] * days

    if days > 5:
        discount = total * 0.10
        total -= discount
        print("Discount: Rs.", discount)

    print("Car:", car_type)
    print("Total Rental Cost: Rs.", total)

calculate_rent()
