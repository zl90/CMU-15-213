# CMU-15-213
Carnegie Mellon University - Introduction to Computer Systems

Course website: https://www.cs.cmu.edu/afs/cs/academic/class/15213-f15/www/
Lecture recordings: https://www.youtube.com/watch?v=4CpHpFu_KYM&list=PLyboo2CCDSWnhzzzzDQ3OBPrRiIjl-aIE&index=2
Textbook: https://www.amazon.com.au/Computer-Systems-Programmers-Randal-Bryant/dp/0134123832/ref=sr_1_3?crid=2KMHE9QBY35Z0&keywords=computer+systems+a+programmer%27s+perspective&qid=1706692019&sprefix=computer+systems%2Caps%2C283&sr=8-3

## Textbook: Computer Systems - A Programmer's Perspective
### Chapter 1
#### 1.9.1 Ahmdah's law - exercises
```
Suppose you work as a truck driver, and you have been hired
to carry a load of potatoes from Boise, Idaho, to Minneapolis,
Minnesota, a total distance of 2,500 kilometers. You estimate
you can average 100 km/hr driving within the speed limits,
requiring a total of 25 hours for the trip.

A. You hear on the news that Montana has just abolished its
speed limit, which constitutes 1,500 km of the trip. Your truck
can travel at 150 km/hr. What will be your speedup for the trip?
```
Answer: Using Ahmdahl's law we can compute the speedup with the formula `S=1/((1-a)+a/k)` where `a` is the fraction of the original time that we are speeding up, and `k` is the performance factor that we are achieving. In this case, `a = 1500/2500 = 0.6` and `k = 150/100`. So the speedup is `S = 1/(0.4+0.6/1.5) = 1.25`. So we can complete the trip in 80% of the original time.

Another way this can be solved is by computing the original time and dividing it by the new time. Original time is 25 hours (2500km at 100km/h), new time is 20 hours (1000km at 100km/h + 1500km at 150km/h). The speedup will be `S = 25 / 20 = 1.25`.
