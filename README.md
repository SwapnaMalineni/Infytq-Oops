class Vehicle:
    def __init__(self,mileage,fuel_left):
        self.mileage=mileage
        self.fuel_left=fuel_left
        self.reserve_fuel=5
    def identify_distance_that_can_be_travelled(self): 
        if self.fuel_left<=self.reserve_fuel:
            return 0
        
        else:
            x=(self.fuel_left-self.reserve_fuel)*self.mileage
            return x
    def identify_distance_travelled(self,initial_fuel):
        return initial_fuel*self.mileage
v=Vehicle(50,10)
print(v.identify_distance_that_can_be_travelled())
print(v.identify_distance_travelled(15))
