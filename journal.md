# this is my journal
    Jan 31st, 2020

1. what did we do? - We learned about the basic rules of computational thinking and how it could be applied to real life situations.
2. what did you learn? I learned that computers don't process and respond to information the same way as humans, and that you have to make extremely specific commands for the computer to process and follow. This can also be applied to real life, as vague information is unacceptable and unrespectful to others, and makes it harder to complete a task.
3. what question do you want to ask? I would like to know a little more about what we are going to study about in this course, specifically the progressions that we'll make as we move on along the year.

#solution to the homework

Here I solved the code challenge:
```.py
triangle(0,0,40,0,0,50);
triangle(40,50,40,0,0,50);
triangle(40,50,0,50,0,100);
triangle(40,50,0,100,40,100);
triangle(40,100,40,75,80,100);
triangle(40,75,80,100,80,75);
```
# This is my journal
    Feb 6th, 2020
1. What did we do? - We did a few commands on how to create different shapes and line between them, as well as how to randomize/make shapes appear as we want, or under a certain amount of time.
2. What did you learn? - I learned that attention to details is very important when doing commands, and that you can modify shapes, their sizes, colors, lines between the shapes.
3. What question do you want to ask? - I would like to ask how we can modify the amount of circles to our own command, like rolling a dice randomly, but the shapes get in a designated place.
# This is my journal
    Feb 10th, 2020
1. What did we do? - We created random amounts of shapes on a designated location, rendering it possible to make a dice and randomize it. We also learned about chance bias, basically making one number more likely to appear than another. We played a game where we had to guess it.
2. What did you learn? - We learned about utilizing the random command to randomize the number of circles but also giving a location to make the circles stay in 1 designed place. We learned about how to make the probability of making 1 number more likely to appear than others.
3. What question do you want to ask? I would like to ask about how to fill color only to the shapes that I want to, for example only filling the circles inside the square but not the square itself.

# This is my journal
    Feb 20th, 2020
1. What did we do? - We did a checkerboard pattern and made the squares move so that it could create an illusion. We made our own illusion as homework.
2. What did you learn? - I learned about how to use the command offset to repeat certain alterations in python.
3. What questions do you have? - I would like to ask what the global command is for.

# This is my journal
    Feb 27th, 2020
1. What did we do? - We showcased our illusions done for homework and made a slideshow about who created the illusion and what makes it an illusion.
2. What did you learn? - I learned about an illusion where the human eye compares relative size of object, therefore certain objects look bigger next to smaller rather than bigger objects.
3. What questions do you have? No comment?

# This is my journal
    March 2nd, 2020
1. What did we do? - We used tinkercad to create a theoretical model of red, green and blue light. We also did coding in order to make the model work.
2. What did you learn? - I learned how to use the delay command so that each light goes off after another like a domino effect.
3. What questions do you have? - I am still oblivious about what most of the objects presented in tinkercad are and their uses, so I would like an explanation of what they are.

# This is my journal
    April 4th, 2020
1. What did we do? - We used a circle to demonstrate a person's location and showed the person's movement by using commands to move it around the background. We also created restrictions for the person so that he wouldn't go away from the screen.
2. What did you learn? - I learned how to program to display an individual's location and their movements, specifically using a circle to demonstrate the location and changing the locations randomly to see movement.
3. What questions do you have?

    solution for the 2 tasks

here I solved the code challenges: 
1.
```.py
#define variables
posx = 300
posy = 300

def setup():
    size (600, 600)
    
def draw():
    global posx, posy
    background (255)
    strokeWeight (2)
    
    #create individual
    circle (posx, posy, 40)
    posx = posx + random (-10,0)
    posy = posy + random (-10,0)
    
    #boundaries conditions
    if posx>580:
        posx=580
    if posy>580:
        posy=580
    if posx<20:
        posx=20
    if posy<20:
        posy=20
        
    delay(100)
```
2.
```.py
#definition of variables
x = []
y = []

def setup():
    size (600, 600)
    for i in range(10):
        x.append(random(0,600))
        y.append(random(0,600))
def draw():
    global x, y
    background (255)
    strokeWeight (2)
    
    #create individuals
    for i in range(10):
        circle (x[i], y[i], 40)
        x[i] = x[i] + random (-10,10)
        y[i] = y[i] + random (-10,10)
    
        #boundaries conditions
        if x[i]>580:
            x[i]=580
        if y[i]>580:
            y[i]=580
        if x[i]<20:
            x[i]=20
        if y[i]<20:
            y[i]=20
        
    delay(100)
```
# This is my journal
    Apr. 15th, 2020
1. How is the e-learning format working for you in our class? - Apart from the fact that I find it hard to figure out the commands on my own, the format is good, including the instructions.
2. is the load sufficient/overwhelming? - I've had not much trouble with the workload up until now, so I'd say it's sufficient.
3. is the format of the video tutorials working? - The video tutorials are working well, however with creating the bar graph and entirely new commands as such, I would suggest that you hint at the research we need to do.
4. Are the meetings meaningful? - The meetings up until now have not been particularly meaningful because what is said in the meeting is already in the online tasks.

    Solution for the tasks:
Here i solved some of the code challenges:
1.
```.py
x = ["bears"]
c = 0

def draw():
    global x
for i in range(100):
    c=c+1
    print c, "bears"
if c == 1:
    print c, "bear"
```
2.
```.py
x = ["the year is"]
c = 1899

def draw():
    global x
for i in range(100):
    c=c+1
    print "the year is", c
```
3.
```.py
x = ["the year is"]
c = -1
f = 0

def draw():
    global x
for i in range(101):
    c=c+1
    f = c*9/5 + 32
    print c, "C are", f, "F"
```
4.
```.py
#definition of variables
x = [100,200]
y = [100,250]
h = [False, True] #False = infected
r = 0
e = 22
f = 0
bar = 0

def setup():
    size (600, 600)
    #create random individuals
    for n in range(20):
        x.append(random(0,600))
        y.append(random(0,600))
        h.append(True) #All healthy 
        barGraph()
        
def distance(x1,x2,y1,y2):
    a = (x1-x2)
    b = (y1-y2)
    c = sqrt(a**2+b**2)
    return c

def draw():
    global x, y, h, r, e, f, bar
    background (255)
    strokeWeight (2)
    barGraph()
    r == 1
    if r == 22:
        e == 1
    
    #ahow the individuals
    for ind in range(len(x)):
        if h[ind]==True:
            fill(255) #healthy
        else:
            fill(255,0,0) #infected 
        circle (x[ind], y[ind], 40)
        #calculate the distance to ach neighbour
        for nei in range (len(x)):
            if nei == ind:
                continue
            d = distance(x[ind], x[nei], y[ind], y[nei])
            if d< 40 and (h[nei] == False or h[ind] == False):
                h[ind] = False
                h[nei] = False
                            
        for m in range (22):
            x[m] = x[m] + random (-10,10)
            y[m] = y[m] + random (-10,10)
    
        #boundaries conditions
            if x[m]>580: 
                x[m]=580
            if y[m]>580:
                y[m]=580
            if x[m]<20:
                x[m]=20
            if y[m]<20:
                y[m]=20
    delay(100)
    
    r = 0
    e = 22
    for bar in range(22):
        if h[bar] == False:
            r +=1
            e -=1
    textSize (20)
    fill (0)
    text ("Infected", 510, 540)
    text ("Healthy", 510, 520)
    text (e, 430, 520)
    text (r, 430, 540)

def barGraph():
    strokeWeight (2)
    stroke (0)
    fill (255, 0, 0)
    rect (500, 530, -r*2, 10)
    fill (255)
    rect (500, 510, -e*2, 10)
```

# This is my journal
    Apr 27th, 2020
1. What did we do?
2. What did you learn?
3. What questions do you have?

Here is my solution for this week's task:
```.py
# definition of variables
x = []
y= []
per = ["Sick", "Healthy"] #Sick=>infected
inf = 0
hel = 25
rec = 0
con = 0
bar = 0
days = [200, -1]

def setup():
    size(500,500)
    for n in range (25):
        x.append(random(0, 500))
        per.append("Healthy") #All Healthy
        y.append(random(0, 500))
        days.append(200)
        barGraph()
        

        
def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c


    
    
def draw():
    global x, y, inf, hel, con, l, days, rec
    background(255)
    strokeWeight(2)
    barGraph()
    con += 1
    if inf == 25:
        con -= 1


    
    #create 1st individual
    for i in range(len(x)):
        if per[i] == "Healthy":
            fill(255) #healthy
        elif per[i] == "Recovered":
            fill(0,255,255)
        else:
            fill (0, 200, 0) #infected
                
        if per[i] == "Sick":
            days[i] -= 1
            if days[i] == 0:
                per[i] = "Recovered"

            
            
        circle(x[i], y[i], 40)
        
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)

        
        for g in range(len(x)):
            if g == i:
                continue
            d = distance(x[i], x[g], y[i], y[g])
            if d < 40 and (per[g] == "Sick" or per[i]== "Sick"):
                if per[i] == "Healthy":
                    #infection happens
                    per[i] = "Sick"
                    days[i] = 200
                if per[g] == "Healthy":        
                    per[g] = "Sick"
                    days[g] = 200

        
        #boundaries conditions
        if x[i] > 500:
            x[i] = 500
    
        # add three more extentions
        
        if x[i] < 0:
            x[i] = 0
            
        if y[i] > 500:
            y[i] = 500
    
        if y[i] < 0:
            y[i] = 0
            
            

            
    inf = 0
    hel = 0
    rec = 0
    for bar in range (len(x)):
        if per[bar] == "Sick":
            inf += 1
        elif per[bar] == "Healthy":
            hel += 1
        elif per[bar] == "Recovered":
            rec += 1

            

            
            
    textSize(10)
    fill(0)
    text("Infected", 445, 478)
    text("Healthy", 445, 458)
    text ("Recovered", 445, 496)
    text (con, 80, 470)
    text("Iteration #:", 20, 470)

            
    

def barGraph():
    strokeWeight(1)
    stroke(0)
    fill(255, 0, 0)
    rect (440, 469, -inf*2, 10)
    fill (255)
    rect (440, 450, -hel*2, 10) 
    fill (0, 255, 255)
    rect (440, 488, -rec*2, 10) 
```
