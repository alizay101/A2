# A2
https://github.com/info-201a-au20/a2-alizay101/blob/master/README.md

a2-core-skills

In this assignment, you'll complete the instructions in the assignment.R file to demonstrate foundational skills of working with R. When you're finished, please make sure to submit this GitHub URL to Canvas on time for full credit.

Assignment 2: Foundational Skills

Before you get started:

- Set your working directory to "source file location" using the Session menu

- Run the following line of code to delete all variables in your workspace

(This will make it easier to test your script)

rm(list = ls())

##Dunzo

Set Up and Defining Variables

Load the stringr package (install it if you haven't used it before)

It has a variety of functions that make working with string variables easier

library(stringr)

Create a variable my_age that is equal to your age

my_age <- 21

Create a variable my_name that is equal to your first name

my_name <- Alizay

Using a multiplication expression, create a variable minutes_in_a_day that

is equal to the number of minutes in a day

minutes_in_a_day <- (60 * 24)

minutes_in_a_day

Using a multiplication expression, create a variable hours_in_a_year that

is equal to the number of hours in a year

hours_in_a_year <- (24 * 365)

hours_in_a_year

Create a variable more_minutes_than_hours that is a boolean (TRUE/FALSE)

It should be TRUE if there are more minutes/day than hours/year

Otherwise, it should be FALSE

more_minutes_than_hours2 <- (minutes_in_a_day < hours_in_a_year) more_minutes_than_hours2

Working with Functions

Write a function named make_introduction() that takes in

two arguments called name and age

This function should return a string value equal to

"Hello, my name is {name}, and I'm {age} years old." but {name} and {age}

should take on the values passed to the function

Make sure that proper spacing is used (e.g., you shouldn't have multiple

spaces between words, and you should have a space after a comma)

Hint: Google search for "R paste paste0 difference"

Try reading a few pages to understand how to use each

make_introduction <- function(statement) { result <- paste(""", statement, "," Hi my name is Alizay, and I'm 21 years old") return(result) }

stm1 <- contradict("19 + 2 = 21") stm2 <- contradict("but you are 20 years old")

cat(stm1) cat (stm2)

contradict3 <- function(statement, person="Alizay") { result <- paste(""", statement, "," ", person, "is not 21 years old") return(result) }

stm1 stm2

Create a variable my_intro by passing your variables my_name and my_age

into your make_introduction() function

my_intro <- make_introduction

my_intro(19-21) my_intro

Create a variable casual_intro by substituting "Hello, my name is",

with "Hey, I'm" in your my_intro variable

a = c("the sky is color", "the color dog", "grass is color") b = c("blue","brown","green") df = data.frame(a,b)

my_intro2 <- {a = c("Hi my name is Alizay") b = c("Hey I'm Alizay") df = data.frame(a, b) }

my_intro2

Create a variable loud_intro, which is my_intro in all upper-case letters

You should do this by using a function to convert your my_intro variable

into all capital letters

my_intro3 <- "Hey my name is Alizay"

answer <- toupper(my_intro)

print(answer)

data.frame(lapply(my_intro, function(v) { if (is.character(v)) return(toupper(v)) else return(v) }))

my_intro

Create a variable quiet_intro, which is my_intro in all lower-case letters

You should do this by using a function to convert your my_intro variable

into all lower-case letters

data.frame(lapply(my_intro, function(v) { if (is.character(v)) return(tolower(v)) else return(v) }))

my_intro

Create a new variable capitalized_intro, which is your my_intro variable

but with each word capitalized

Hint: Google search the stringr function str_to_title

demo1 <- "hey my name is alizay" str_to_title(demo1)

str_to_title(my_intro)

Using the str_count function from stringr, create a variable occurrences

that stores the # of times the letter "e" appears in my_intro

str_count(string = my_intro, pattern = "e") str_count(string = my_intro, pattern = "i")

Write a function double() that takes in a value and

returns that value multiplied by 2

the_double <- function(a) { answer <- (a * 2) return(answer) }

the_double(2) the_double(6)

Using your double() function, create a variable minutes_in_two_days,

which is the number of minutes in two days

the_double()

minutes_in_two_days <- the_double(1440)

minutes_in_two_days

minutes_in_two_days <- the_double(minutes_in_a_day)

Write a function cube() that takes in a value and returns that value cubed

the_cubed <- function(x) { answer <- (x * x) return(answer) }

the_cubed(4) the_cubed()

Create a variable twenty_seven by passing 3 to your cube() function

twenty_seven <- function(x) { answer <- (x * x * x) return(answer) }

twenty_seven(3*1)

the_cubed(3*9)

Create a function inches_to_cm that converts from inches to centimeters

inches_to_cm <- function(a) { answer <- (a * 2.54) return(answer) }

inches_to_cm(2)

Create a variable inches_tall that is your (numeric) height in inches

inches_tall <- 67

Using your inches_to_cm function and your inches_tall variable,

create a variable cm_tall that is your height in centimeters

cm_tall <- inches_to_cm(inches_tall)

cm_tall

Write a function has_more_zs to determine which of two strings contains

more instances of the letter "z". It should take as parameters two string

variables and return the argument which has more occurrences of "z"

If neither phrase contains the letter "z", it should return:

"Neither string contains the letter z."

If the phrases contain the same number of "z"s, it should return:

"The strings have the same number of Zs."

The function must work for both capital and lowercase "z"s.

nchar(my_intro)

x = c("Alizay", "Zayn", "Ali", "Alice", "Musa") x[grep("^A",x)]

x2 <- my_intro

x2[grepl("(?i)*z",x2)]

example1 <- "the zoo has a zebra" example1

example2 <- "Alizay is going to the zoo to see the zebra" example2

length(example1)

has_more_zs <- (example1 < example2) { print("has more z's") }

example1.1 <- 2 example2.1 <- 3

if(example1 >= example2) { print("Neither string contains the letter z") }

if(example1 >= example2) { print("You have no z's") } else { print("There are too many z's : (") }

Create a variable more_zs by passing two strings of your choice to your

has_more_zs function

if(example1 >= example2) { print("Neither string contains the letter z") }

if(example1 >= example2) { print("You have no z's") } else { print("There are too many z's : (") }

Write a function remove_digits that will remove all digits

remove_digits <- function(x) { answer <- (x- x) return(answer) }

remove_digits(2)

remove_digits(inches_tall)

(i.e., 0 through 9) from all elements in a vector of strings.

x <- c("alizay45", "alizay100") removeNumbers(x)

remove_digits <- removeNumbers

remove_digits(x)

Demonstrate that your approach is successful by passing a vector of courses

to your function. For example, remove_digits(c("INFO 201", "CSE 142"))

demo3 <-c ("info 201", "Info 496", "CSE 142")

remove_digits(demo3)

Vectors

Create a vector movies that contains the names of six movies you like

ordered_movies <- c(1, 2, 3, 4, 5) movies <- c("Dil Se", "Pans Labyrinth", "Doctor Sleep", "Coraline", "Nightmare Before Christmas")

Create a vector top_three that only contains the first three movies of

your movies list (e.g., index 1 through index 3)

top_three <- c("Dil Se", "Coraline", "Pans Labyrinth")

movies[c(1, 2, 4)]

Using your vector and the paste() method, create a vector excited that

adds the phrase " is a great movie!" to the end of each element in movies

paste( c("Dil se", "Coraline", "Pans Labyrinth"), c("is a great movie!", "is a great movie!", "is a great movie!") )

Create a vector without_four that omits the fourth element from movies

You should do this by using a negative index

without_four <- movies[-4] without_four

Create a vector multiples_of_4 that is every number divisible by 4

between 4 and 400 (2 points)

multiples_of_4 <- input[(input %% 4) == 0]

Create a vector multiples_of_8 by filtering your multiples_of_4 variable

down to only elements that are divisible by 8.

Hints:

- See chapter 7.4 in the book for vector filtering

- Google search "modulo operator in R"

multiples_of_8 <- input[(input %% 8) == 0]

multiple_of_4 > 322%%8

multiple_of_8_d <- multiple_of_4[-4]

multiple_of_8_d

Create a vector numbers that is the numbers 700 through 999

numbers <- c(700:999)

numbers

Using the built in length() function, create a variable numbers_len

that is equal to the length of the vector numbers

numbers_len <- length(numbers) = numbers

numbers_len

Using the mean() function, create a variable numbers_mean that is

equal to the mean of the vector numbers

numbers_mean <- mean(700:999)

numbers_mean

Using the median() function, create a variable numbers_median

that is the median of the vector `numbers

numbers_median <- median(700:999)

numbers_median

Create a vector lower_numbers that the values in the numbers vector

that are lower than numbers_mean

Hint: Use vector filtering)

lower_numbers <- function(numbers) { if (X==numbers_mean) return(TRUE) else return(FALSE) }

lower_numbers

Create a vector higher_numbers that the values in the numbers vector

that are higher than numbers_mean

Hint: Again, use vector filtering

higher_numbers <- function(numbers) { if (X==999) return(TRUE) else return(FALSE) }

higher_numbers(999)

Lists

Create a list called summary_info in which you'll store summary information

about the numbers vector above.

The list should contain the following named keys:

- length: in which you'll store the length of the vector

- mean: in which you'll store the mean of the vector

- median: in which you'll store the median of the vector

summary_info <- list(1, "2", TRUE) length <- 306 mean <- 849.5 median <- 849.5

Now, write a function called summarize_vector that takes in a vector of

numbers, and returns a list of summary information about that vector

(including the mean, median, and length)

summarize_vectors <- list(mean = 849.5, length = 306, median = 849.5)

summarize_vectors

summarize_vectors$mean summarize_vectors$length summarize_vectors$median

Create a list summary_1_to_100 by passing a vector of the values one

through one hundred to your summarize_vector function

summary_1_100 <- list(summarize_vectors)

summary_1_100

Data Frames

Create a vector students holding 1,000 values representing students

They should have the values "Student 1", "Student 2",..., "Student 1000"

students <- seq(from = 1, to = 1000, length.out = 1000)

students

set.seed(1)

sample(1:1000, 10, replace = TRUE)

Create a vector math_grades that holds 1000 random values in it that

represent grades in a math course

These values should be normally distributed with a mean of 88 and a

standard deviation of 10

Hint: Lookup rnorm()

math_grades <- rnorm(1000, mean = 88, sd = 10)

math_grades

In the math_grades vector, replace any values that are above 100 with

the number 100

Hint: Vector filtering

math_grades <- rnorm(1000, mean = 88, sd = 10)

math_grades

math_grades2 <- function(math_grades) { if (math_grades==100) return(100) else return(FALSE) }

math_grades2(87)

Create a vector spanish_grades that holds 1000 random values in it that

represent grades in a spanish course

These values should be normally distributed with a mean of 85 and a

standard deviation of 12

Hint: Lookup rnorm()

spanish_grades <- rnorm(1000, mean = 85, sd = 12)

spanish_grades

In the spanish_grades vector, replace any values that are above 100 with

the number 100

Hint: More vector filtering

spanish_grades2 <- function(spanish_grades2) { if (spanish_grades2==100) return(100) else return(FALSE) }

spanish_grades2(87)

Create a data frame variable named grades by combining

the vectors students, math_grades, and spanish_grades

Make sure to properly handle strings

grades.data <- data.frame(spanish_grades, math_grades)

grades.data

Create a variable num_students that counts the

number of rows in your dataframe grades

num_students <- nrow(grades.data) num_students

Create a variable num_courses that counts the number of courses stored

in the columns of your grades data frame

num_courses <- ncol(grades.data) num_courses

Add a new column grade_diff to your data frame, which is equal to

grades$math_grades minus grades$spanish_grades

grade_diff["grade_difference"] <- (math_grades - spanish_grades)

grade_diff

Add another column better_at_math as a boolean (TRUE/FALSE) variable that

indicates that a student got a better grade in math

better_at_math <- (math_grades >= spanish_grades) better_at_math

Create a variable num_better_at_math that is the number

(i.e., one numeric value) of students better at math

num_better_at_math <- (better_at_math[c(1)]) num_better_at_math

num_better_at_math <- sum(better_at_math) num_better_at_math
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
