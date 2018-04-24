**You're about to get on a plane to Seattle. You want to know if you should bring an umbrella. You call 3 random friends of your who live there and ask each independently if it's raining. Each of your friends has a 2/3 chance of telling you the truth and a 1/3 chance of messing with you by lying. All 3 friends tell you that "Yes" it is raining. What is the probability that it's actually raining in Seattle? **

```
 Bayesin Theorem: P(H | E) = P(E | H) * P(H) / P(E)  
 0.25*(2/3)^3 + 0.75*(1/3)^3 = 0.25*(8/27) + 0.75*(1/27)
 0.25*(8/27) / (0.25*8/27 + 0.75* 1/27)
 All the 27 cancel each other out, so multiply the bottom and the top by 4.
 8/(8+3) = 8/11.
```



**A Russian gangster kidnaps you. He puts two bullets in consecutive order in an empty six-round revolver, spins it, points it at your head and shoots. \*click\* You're still alive. He then asks you, do you want me to spin it again and fire or pull the trigger again. For each option, what is the probability that you'll be shot?**

```
1/4 for pulling the trigger. 1/3 for spinning and pulling the trigger. 
```



