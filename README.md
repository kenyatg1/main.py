import math

print("Hello Console!")

my_name = "Kenyat"
work_from_home = False
side = 15
radius = 10
print("My name is " + my_name)
print("I work from home: " + str(work_from_home))
print(f"The length of each side of the square is {side}")
txt = "The radius of the circle is {}"
print(txt.format(radius))

square_area = side * side
square_perimeter = 4 * side
circle_area = radius * radius * math.pi
circle_perimeter = 2 * math.pi * radius
print(f"The square area is {square_area} and the perimeter is {square_perimeter}")
print(f"The circle area is {circle_area} and the circle perimeter is {circle_perimeter}")

travel_options = ["foot", "bike", "car", "airplane"]
print("The travel options are:")
print(f"1) {travel_options[0]}")
print(f"2) {travel_options[1]}")
print(f"3) {travel_options[2]}")
print(f"4) {travel_options[3]}")
travel_type = input("How would you like to travel?" )
print ("Travel type: " + travel_type)
distance = 100
time = 0
cost = 0
if travel_type == "foot":
    print("Walking is free! Speed is 3mph.")
    cost = 0
    time = distance/3
elif travel_type == "bike":
    rent_bike = input("Do you need to rent the bike? (yes or no)")
    if rent_bike == "yes":
        print("Bike rental is $45! Speed is 10mph")
        cost = 45
else:
    print("Biking is free! Speed is 10mph.")
    cost = 0
    time = distance/10
if travel_type == "car":
    print("Driving is $.25/mi. Speed is 60mph.")
    cost = .25 * distance
    time = distance/60
if travel_type == "airplane":
    print("Flying is $.10/mi Speed is 400mph.")
    passenger_count = int(input("How many passengers?"))
    cost = .10 * distance * passenger_count
    time = distance/400
else:
    print(f"Sorry. {travel_type} is an invalid option.")

print(f"Traveling {distance} miles by {travel_type} took {time} hours and cost ${cost}")
