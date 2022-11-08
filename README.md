class hamster:
    def __init__(self,name):
        self.name= name
        self.hunger=0
        self.mood="happy"
        self.bored=0
    def eat(self):
        self.hunger+=int(input("enter number for food"))  
    def update(self):
        self.hunger-=10
        self.bored-=10
        if self .hunger<0 or self.bored<0:
            self.mood="grumpy"
        elif self.hunger<20:
            self.mood="happy"
        else:
            self.mood = "ecstatic"
    def printInfo(self):
        print("my name is" ,self.name,"and i am ",self.mood)

pet1= hamster("DULCE")
pet2= hamster("ARALY")
pet3= hamster("JAZMIN")
print("welcome to the hamster simulator")
print()



while True:
    choice=int(input("press 1 to feed DULCE, press 2 to feed ARALY,press 3 to feed JAZMIN and 4 to print INFO"))
    if choice==1:
        pet1.eat()
    elif choice==2:
        pet2.eat()
    elif choice==3:
        pet3.eat()
    else:
        pet1.printInfo()
        pet2.printInfo()
        pet3.printInfo()
        
        
    pet1.update()
    pet2.update()
    pet3.update()
