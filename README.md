# Spark

## About Me and the Objective 

I am Hitesh Kolla pursuing my masters in Northwest missouri state university. I am doing this project as a part of my "BigData" course. The main objective of the project is to find the most commonly used words using the joker story in Batman. Spark is used to do overall project.

## Data
I took data the from wikipedia about joker character in a movie batman. From the wikipedia I just want to find the most frequently used  words. So with the help of most commonly repeated words and the count of the words, we can represent them graphically. Now here I considered the wordcount of most frequently used words. I used it in tableau where the data can be analysied perfectly in graphs formats.  
Source : https://en.wikipedia.org/wiki/Joker_(character)

## Commands:

> val inputFile = sc.textFile("C:/44517/spark.txt")  
> val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);  
> counts.saveAsTextFile("c:/output")  

## Results

Here is the result that is obtained by using the above commands  

| Word    | Count|
|---------|------|
| the     | 29   |
| and     | 20   |
| joker   | 16   |
| in      | 14   |
| of      | 13   |
| The     | 12   |
| his     | 11   |

From the above result i.e., In tableau it considers the case too. It shows the word "The" has two different ones as "The" and"the". 
and the most repeated word is "the" and the least reapeated word is "his".
  
 ### Bar graphs:  
![final](https://user-images.githubusercontent.com/31717045/48322608-10b3dc00-e5ee-11e8-819a-f51fa3057316.PNG)

