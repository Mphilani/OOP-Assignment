# OOP-Assignment
class Smartphone:
    def __init__(Peeps, brand, model, battery_life):
        Peeps.brand = brand          
        Peeps.model = model          
        Peeps.battery_life = battery_life  
    
    def display_info(Peeps):
        print(f"Smartphone: {Peeps.brand} {Peeps.model}")
        print(f"Battery Life: {Peeps.battery_life} hours")
    
    def charge(Peeps):
        print(f"{Peeps.brand} {Peeps.model} is now charging...")
    
    def use_app(Peeps, app_name):
        print(f"Using {app_name} on {Peeps.brand} {Peeps.model}...")

class GamingPhone(Smartphone):
    def __init__(Peeps, brand, model, battery_life, cooling_system):
        super().__init__(brand, model, battery_life) 
        Peeps.cooling_system = cooling_system   

    def display_info(Peeps):
        """Override to include the cooling system"""
        super().display_info()
        print(f"Cooling System: {Peeps.cooling_system}")

smartphone = Smartphone("Apple", "iPhone 14", 20)
gaming_phone = GamingPhone("Asus", "ROG Phone 5", 18, "Active Cooling")


smartphone.display_info()
gaming_phone.display_info()

smartphone.use_app("Instagram")
gaming_phone.charge()

class Vehicle:
    def move(Traveller):
        """General method for moving (to be overridden)"""
        pass
# OOP-Assignment//Polymorphism Challenge!
class Car(Vehicle):
    def move(Traveller):
        print("Driving ")

class Plane(Vehicle):
    def move(Traveller):
        print("Flying ")

class Bicycle(Vehicle):
    def move(Traveller):
        print("Pedaling ")

car = Car()
plane = Plane()
bicycle = Bicycle()

car.move()      
plane.move()    
bicycle.move()  
