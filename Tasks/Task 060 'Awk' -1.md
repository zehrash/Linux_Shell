## 'Awk' -1

[Judge System](https://www.hackerrank.com/challenges/awk-1/problem)

#### Objective 
In this challenge, we practice using the awk command for text-munging and data processing tasks.

#### Resources 
Here's a useful video on the topic:

[VIDEO](https://youtu.be/az6vd0tGhJI)

The awk interpreter may be used for a lot of text-munging and data-processing tasks that require some quick scripting work.

The following links show examples with awk:

[Print Examples](https://www.thegeekstuff.com/2010/01/awk-introduction-tutorial-7-awk-print-examples/)<br>
[Conditionals with Awk](https://www.thegeekstuff.com/2010/02/awk-conditional-statements/)

#### Task 

You are given a file with four space separated columns containing the scores of students in three subjects. The first column contains a single character (<img src="https://latex.codecogs.com/svg.latex?\Large&space;A-Z">), the student identifier. The next three columns have three numbers each. The numbers are between <img src="https://latex.codecogs.com/svg.latex?\Large&space;0"> and <img src="https://latex.codecogs.com/svg.latex?\Large&space;100">, both inclusive. These numbers denote the scores of the students in English, Mathematics, and Science, respectively.
Your task is to identify those lines that do not contain all three scores for students.

#### Input Format

There will be no more than <img src="https://latex.codecogs.com/svg.latex?\Large&space;10"> rows of data.<br>
Each line will be in the following format:<br>
[Identifier][English Score][Math Score][Science Score]

#### Output Format

For each student, if one or more of the three scores is missing, display:

```
Not all scores are available for [Identifier]
```

#### Sample Input

```
A 25 27 50
B 35 75
C 75 78 
D 99 88 76
```

#### Sample Output

```
Not all scores are available for B
Not all scores are available for C
```

#### Explanation
Only <img src="https://latex.codecogs.com/svg.latex?\Large&space;2"> scores have been provided for student B and student C.