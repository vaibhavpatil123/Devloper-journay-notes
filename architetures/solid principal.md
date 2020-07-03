https://www.youtube.com/watch?v=rtmFCcjEgEw&t=415s


1. Responsibility separation 
Clean and define responsibility to class 
Popjones
2. Open for extension and close for modification
- add new things without change of old one
- separate the behaviors to easily expand system
Near break core functions with new changes 

Example - Open source lib , use factoty pattern class instance on run time 

interface payble interface 
and 3 extend interfaces for types -paypal, paytm and atm
Factory method to initalise 

 3. LisKov substation principle 
- Derived class should replace parent class without consumer know it 
Example - Database engine changes , interface DAO and DB Dao implements 

RubberDuck extend Duck (quack.fly and swim methods)
override all method - not good 
Good design - split methods in 3 interfaces QuckableInterface ,Swimmable and FlyableInterface 

So RubberDuck now will implement requried interface 

"Program work correctly in some cases and conditionally "
"Method should work for intent that expects"

4 Interface segregation principle 
-Client never force to depends on method he don’t use

"HeadSet with more than headset interfaces"

Interface Notification 
subscriber 
unsubscribe 

Now if we have NotifcationClass which depends on SubscriberInf and we added new things then it will impact NotifcatioNClass also 
Split interface and break into more interface 

Keep balance separation 

5. Dependency inversion Principal 

Interface is socket and plug - Abstraction part 
Change in bag round and really on abstractions

Solid is tool , principal and not rule , better code and raiser and maintain code 


