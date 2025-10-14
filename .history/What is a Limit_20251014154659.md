Hello class!

Today, we're going to dive into the world of **limits**, a fundamental concept in calculus. Up until now, we've been focused on evaluating a function, let's say 

f, at a specific x-value1. For example, if we have 



f(x)=x+2, we'd find f(3) by simply plugging in 3 to get 3+2=5.

Limits are different. Instead of looking at a single point, we're going to look at the 

**behavior of a function near a certain x-value**2. This is called "the limit of 



f(x) as x approaches a," and it's a critical concept for understanding things like instantaneous rates of change later on3.





### What is a Limit?



------

Think of it like this: A limit is the value a function gets closer and closer to as the x-value gets closer and closer to a certain number4. It's about where the function is 



**headed**, not necessarily where it is when it gets there5.



We write this as:





limx→af(x)=L 6



This is read as "the limit of 

f(x), as x approaches a, equals L." 7



An important thing to remember is that the limit of 

f(x) as x approaches a has nothing to do with what the function actually is at f(a)8. The limit can exist even if the function is undefined at that point9.



Let's look at an example to make this clearer.

Consider the function 

f(x)=x−1x2+x−210. If we try to find 



f(1), we get 00, which is undefined1111. However, we can still find the limit as 



x approaches 1.

For any x that isn't 1, we can simplify the function by factoring the top:





f(x)=x−1(x−1)(x+2)=x+2 12



So, our function is really the line 

y=x+2, but with a hole at x=113. As we can see from the graph 14, as 



x gets closer to 1 from both the left and the right side, the value of the function gets closer and closer to 315. Therefore, even though 



f(1) is undefined, the limit as x approaches 1 is 316.





limx→1f(x)=3. 17



A limit might also not exist at all, for instance if the function goes to infinity18181818. Take the function 



f(x)=x2119. As 



x gets closer to 0 from either side, the value of f(x) gets "arbitrarily large"20. It doesn't approach a specific finite number, so the limit does not exist21. We can also write this as 



limx→0f(x)=∞22.





### One-Sided Limits



------

Sometimes, we need to consider the limit from only one side.

- A **left-hand limit** means we're looking at what happens to the function as x approaches a from values **less than** a. We write this as 

  limx→a−f(x)=L23.

  

  

- A **right-hand limit** means we're looking at what happens as x approaches a from values **greater than** a. We write this as 

  limx→a+f(x)=L24.

  

  

For a full, two-sided limit to exist, the left-hand and right-hand limits must both exist and be equal2525.



Let's look at the function 

g(x) in the provided graph26262626.



- As 

  x approaches 2 from the left (from values less than 2), the function approaches a y-value of 3. So, limx→2−g(x)=327.

  

  

- As 

  x approaches 2 from the right (from values greater than 2), the function approaches a y-value of 1. So, limx→2+g(x)=128.

  

  

- Since the left and right-hand limits are not equal, the two-sided limit at 

  x=2 **does not exist**29292929.

  

  

  



### Limit Laws



------

Just like we have rules for algebra, we have a set of rules for working with limits, called 

**limit laws**30. If 



limx→af(x)=A and limx→ag(x)=B, and c is a constant, then:

- 

  **Sum/Difference:** limx→a[f(x)±g(x)]=A±B 31

  

  

- 

  **Constant Multiple:** limx→a[c⋅f(x)]=cA 32

  

  

- 

  **Product:** limx→a[f(x)⋅g(x)]=AB 33

  

  

- 

  **Quotient:** limx→ag(x)f(x)=BA as long as B=0 34

  

  

- 

  **Power:** limx→a(f(x)r)=Ar 35

  

  

- 

  **Constant:** limx→ac=c 36

  

  

- 

  **Identity:** limx→ax=a 37

  

  

These laws also apply to one-sided limits, as long as all the limits are taken from the same side38.



For many functions, you can find the limit by simply plugging the value of a into the function. This is called the 

**Direct Substitution Property**39. It works for polynomials and rational functions as long as 



a is in the domain of the function40.



For example, to find 

limx→2x+1x−3, you can just substitute x=2 since it is in the domain of the function414141.





limx→2x+1x−3=2+12−3=−31 42



However, as we saw in our first example, direct substitution doesn't always work if you get an undefined result like 

0043434343. In those cases, you have to do some algebraic manipulation first. For example, if you encounter a square root in the expression, you can try multiplying the top and bottom by the "square root conjugate" to simplify it44444444.



For more practice with these concepts, we can work through some of the extra problems in the notes. Any questions so far?