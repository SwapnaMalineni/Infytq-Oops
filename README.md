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

class Vehicle:
  def __init__(self):
    self.__vehicle_id = None
    self.__vehicle_cost = None
    self.__vehicle_type = None
    self.__premium_amount = None
  
  def get_vehicle_id(self):
    return self.__vehicle_id
  def set_vehicle_id(self, vehicle_id):
    self.__vehicle_id = vehicle_id

  def get_vehicle_cost(self):
    return self.__vehicle_cost
  def set_vehicle_cost(self, vehicle_cost):
    self.__vehicle_cost = vehicle_cost

  def get_vehicle_type(self):
    return self._vehicle_type
  def set_vehicle_type(self, vehicle_type):
    self.__vehicle_type = vehicle_type

  def get_premium_amount(self):
    return self.__premium_amount
  def set_premium_amount(self, premium_amount):
    self.__premium_amount = premium_amount

  def calculate_premium(self):
    if self.__vehicle_type == "Two Wheeler":
      self.__premium_amount = (2/100)*self.__vehicle_cost
    elif self.__vehicle_type == "Four Wheeler":
      self.__premium_amount = (6/100)*self.__vehicle_cost
    else:
      print("Vehicle type is Invalid")

  def display_vehicle_details(self):
    print("vehicle id : ",self.__vehicle_id)
    print("vehicle type : ",self.__vehicle_type)
    print("vehicle cost : ",self.__vehicle_cost)
    print("premium amount : ",self.__premium_amount)

car = Vehicle()
car.set_vehicle_id(100)
car.set_vehicle_type("Four Wheeler")
car.set_vehicle_cost(600000)
car.calculate_premium()
car.display_vehicle_details()
