### Practical1: Using R execute the basic commands, array , list and frames

``` 
num_vec <- c(1, 2, 3, 4, 5)
char_vec <- c("apple", "banana", "cherry")
print(num_vec)
print(char_vec)
print(class(num_vec))
print(class(char_vec))

#matrix command
mat <- matrix(1:9, nrow = 3, ncol = 3)
print(mat)
print(class(mat))

#list command
my_list <- list(1, "apple", TRUE, 3 + 4i)
print(my_list)
print(class(my_list))

#dataframes
df <- data.frame(
  numbers = c(1, 2, 3),
  fruits = c("apple", "banana", "cherry"),
  logicals = c(TRUE, FALSE, TRUE)
)


print(df)
print(class(df))
```

### Practical2: Create matrix using R and perform the operation addition, multiplication, division

```
#Creating First matrix  
#Creating First matrix  
myMatrixA <- matrix(c(1, 2, 3, 4, 5, 6,7,8,9), nrow = 3, ncol = 3)   
myMatrixA 

#Creating Second matrix  
myMatrixB <- matrix(c(9,8,7,6,5,4,3,2,1), nrow = 3, ncol = 3)   
myMatrixB  

#Adding Both Matrices  
myMatrixCAfterAdding <- myMatrixA + myMatrixB  
myMatrixCAfterAdding

#Subtracting Both Matrices  
myMatrixCAfterSubtract <- myMatrixA - myMatrixB  
myMatrixCAfterSubtract 
 

#Creating matrices
matrixm<- matrix(1:8, nrow=2)
matrixm
matrin<- matrix(8:15, nrow=2)
matrin

#Multiplying matrices
myMatrixCAfterMultiply <- myMatrixA * myMatrixB  
myMatrixCAfterMultiply

#Creating matrices
matrixm<- matrix(1:8, nrow=2)
matrixm
matrixn<- matrix(8:15, nrow=2)
matrixn

#division matrices  
myMatrixCAfterDivide <- myMatrixA / myMatrixB  
myMatrixCAfterDivide

```

### Practical 3:Using R studio calculate mean median mode.

```
#Taking a list of elements
list = c(2, 4, 4, 4, 5, 5, 7, 9)

#Calculating average using mean()
print(mean(list))

#R program to get variance of a list

#Taking a list of elements
list = c(2, 4, 4, 4, 5, 5, 7, 9)

#Calculating variance using var()
print(var(list))

#R program to get 
#standard deviation of a list

#Taking a list of elements
list = c(2, 4, 4, 4, 5, 5, 7, 9)

#Calculating standard 
#deviation using sd()
print(sd(list))
```

### Practical4: Using R import the data from excel/.CSV file and performs above function

```
> library(readxl)
> data <- read_excel("C:/Users/ITL1PC8/Desktop/data.xlsx")
> View(data)
mean(data$Spades)
mode(data$Spades)
median = median(data$Spades)
print(median)mode(data$Spades)
```

### Practical5:  Using R import the data from excel/.CSV file and performs data standard deviation

```
> library(readxl)
> data <- read_excel("C:/Users/ITL1PC8/Desktop/data.xlsx")
> View(data)
var(data$Spades)
sd(data$Spades)
```

### Practical 6: :  Using R import the data from excel/.CSV file and draw the skewness.

```
install.packages("e1071")
library(e1071)

#Example data
	data <- c(2, 3, 5, 6, 8, 9, 12, 15, 18, 21)
	
#Calculate skewness
skewness_value <- skewness(data)
print(skewness_value)
hist(data)
install.packages("e1071")
library(e1071)

#positive skew
x <- c(30, 31, 32, 33, 40)
skewness_value <- skewness(x)
print(skewness_value)
hist(x)
```

### Practical 7: :  Using R import the data from excel/.CSV file and performs hypothetical testing

```
#Read data with CSV
input<-read.csv("D:/SYIT COST PRACT/Prac/P7DATA.csv")

#Without excel use this method to get same result of input
#input<-data.frame(Finance = c(12,7),Sales = c(38,19), HR=c(5,3), Technology=c(8,1))

View(input)
attach(input)
result<-chisq.test(input)
print(result)
if(result$p.value>=0.05){
  print("Null Hypothesis is Accepted")
}else{
  print("Null Hypothesis is Rejected")
}
```

### Practical 8: Using R perform the binomial and normal distribution on the data.

```
#Suppose the number of games in which major league baseball players play 
#during their careers is normally distributed with mean equal to 1500 games,
#standard deviation equal to 350 games. Use R to solve the following problems.
#(a) What percentage play in fewer than 750 games? 
#(b) What percentage play in more than 2000 games?
#(c) Find the 90th percentile for the number of games played during a career.

print("What percentage play in fewer than 750 games")
pa<-pnorm(750, mean = 1500, sd = 350)
Percenta <- pa*100
print(Percenta)

print("What percentage play in more than 2000 games")
pb<-pnorm(2000, mean = 1500, sd = 350, lower.tail = FALSE)
Percentb <- pb*100
print(Percentb)

print("the 90th percentile for the number of games played during a career (range)")
p05<-round(qnorm(0.05,mean = 1500, sd = 350),0)
p95<-round(qnorm(0.95,mean = 1500, sd = 350),0)

cat("Range for 90 Percentile is : ",p05,"-",p95)

p90<-round(qnorm(0.90,mean = 1500, sd = 350),0)
cat("exact value :",p90)
```
