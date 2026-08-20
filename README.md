# P4
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):
        print("Dog says Woof")

class Cat(Animal):
    def sound(self):
        print("Cat says Meow")

animals = [Dog(), Cat()]

for animal in animals:
    animal.sound()



    class Payment:
    def pay(self, amount):
        print("Processing payment of ₹", amount)


class UPI(Payment):
    def pay(self, amount):
        print("Paid ₹", amount, "using UPI")


class CreditCard(Payment):
    def pay(self, amount):
        print("Paid ₹", amount, "using Credit Card")


class Cash(Payment):
    def pay(self, amount):
        print("Paid ₹", amount, "using Cash")


amount = float(input("Enter amount: "))

print("1. UPI")
print("2. Credit Card")
print("3. Cash")

choice = int(input("Enter your choice: "))

if choice == 1:
    payment = UPI()
elif choice == 2:
    payment = CreditCard()
elif choice == 3:
    payment = Cash()
else:
    print("Invalid choice")
    exit()

payment.pay(amount)
