# Homework2
the dice is assumed to be roll 100 times
the probability is 1/6 for any outcome so the sum is 6

The Hypotheis is H0: p1=p2=p3=p4=p5=p5
                 Ha: there is a difference
                 
The test used is the test of goodness of fit
the significance level is 0.05.
# so here is the console part
 dice<-sample(1:6,100,TRUE)
> dice==1
  [1] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [14] FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [27] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE
 [40] FALSE  TRUE  TRUE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE
 [53]  TRUE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE
 [66] FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE  TRUE FALSE FALSE FALSE
 [79] FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE
 [92] FALSE FALSE FALSE FALSE  TRUE  TRUE FALSE FALSE FALSE
> summary(dice==1)
   Mode   FALSE    TRUE 
logical      87      13 
> summary(dice==2)
   Mode   FALSE    TRUE 
logical      86      14 
> summary(dice==3)
   Mode   FALSE    TRUE 
logical      85      15 
> summary(dice==4)
   Mode   FALSE    TRUE 
logical      85      15 
> summary(dice==5)
   Mode   FALSE    TRUE 
logical      79      21 
> summary(dice==6)
   Mode   FALSE    TRUE 
logical      78      22 
> Obs_value1=14
> Obs_value2=16
> Obs_value3=16
> Obs_value4=19
> Obs_value5=21
> Obs_value6=14
> sum(Obs_value1,Obs_value2,Obs_value3,Obs_value4,Obs_value5, Obs_value6)
[1] 100
> Exp_value= 100*(1/6)
> #lets use the Chisquare test of goodness of fitted
> #let us state the Hypothesis
> ##H0: p1=p2=p3=p4=p5=p6 
> ##Ha:there is a difference somewhere
> #let us calculate the chisquare as X
> X<-((Obs_value1- Exp_value)^2 /(Exp_value))+((Obs_value2- Exp_value)^2 /(Exp_value))+((Obs_value3- Exp_value)^2 /(Exp_value))+((Obs_value4- Exp_value)^2 /(Exp_value))+((Obs_value5- Exp_value)^2 /(Exp_value))+((Obs_value6- Exp_value)^2 /(Exp_value))
> X
[1] 2.36
> 
> #now let us compare my X chisquare to the Chisquare with alpha=0.10, 0.05 and 0.01
> #Xalpla at 0.10 = 9.236, so we conclude that we cannot reject the null hypothesis.
> #so, there is evidence that at 95% that the dice is fair. Xalpha>Xcalculate.



THE SECOND TRIAL FOR THE FILE HOMEWORK2 PROPER


> # H0: p1=p2=p3=p4=p5=p6
> # Ha: there is a difference
> # Alpha=0.10
> dices<-sample(1:6,100,TRUE)
> summary(dices==1)
   Mode   FALSE    TRUE 
logical      86      14 
> summary(dices==2)
   Mode   FALSE    TRUE 
logical      86      14 
> summary(dices==3)
   Mode   FALSE    TRUE 
logical      81      19 
> summary(dices==4)
   Mode   FALSE    TRUE 
logical      84      16 
> summary(dices==5)
   Mode   FALSE    TRUE 
logical      84      16 
> summary(dices==6)
   Mode   FALSE    TRUE 
logical      79      21 
> 
> dicerf<-c(15,24,20,14,12,15)
> res<-chisq.test(dicerf,p= c(1/6,1/6,1/6,1/6,1/6,1/6))
> res

	Chi-squared test for given probabilities

data:  dicerf
X-squared = 5.96, df = 5, p-value = 0.3101

> 
> #the level of significance is aplha= 0.10
> ##p-value> alpla , that means the dice is unfair at a 90% confidence level






