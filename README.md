# stephen1new
die<-1:6
roll<-function(){
  dice<-sample(die,size=3,replace=TRUE,prob = c(0.5,0.1,0.1,0.1,0.1,0.1))
  sum(dice)
}

chance<-replicate(1000,roll())
qplot(chance,binwidth=1)

