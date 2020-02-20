# stephen1new
#creating a 2 by 3 named object die
die<-1:6
names(die)<-c("one","two","three","four","five","six")
dim(die)<-c(2,3)

#creating a function that rolls the die and selects three values using the given probabilities and adding up the sums of the numbers
roll<-function(){
  dice<-sample(die,size=3,replace=TRUE,prob = c(0.5,0.1,0.1,0.1,0.1,0.1))
  sum(dice)
}

#replicating the rolls 1000 times and visualises the numbers
chance<-replicate(1000,roll())
qplot(chance,binwidth=1)

