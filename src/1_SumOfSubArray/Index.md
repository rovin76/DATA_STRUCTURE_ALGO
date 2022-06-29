## Noddy's Examination -112:39:36

# Description

Noddy has an exam in which each question has a difficulty level in the form of an Integer. Now, Noddy can only solve the problems that have difficulty level less than or equal to X. Now the rules are-

The score of the student is equal to the maximum number of answers he/she has attempted without skipping a question.

The student is allowed to skip just "one" question that will not be counted in the continuity of the questions.

Note- Assume the student knows the solution to the problem he/she attempts and always starts the paper from the first question.

Given the number of Questions, N, the maximum difficulty level of the problem Noddy can solve, X, and the difficulty level of each question in the form of an array

Determine the maximum score that Noddy can score?

- Input

First Line contains Integer N, the number of questions and the maximum difficulty X Noddy can solve.

Next line contains N integers, denoting the difficulty level of each question.

N <= 100000

X <= 1000000000

Difficulty level of each question <= 1000000000

- Output
  Print the maximum score that Noddy can score

```
Sample Input 1

7 6
4 3 7 6 7 2 2

```

Sample Output 1

```
3

```

- Hint

Sample 1 Explanation

### Code

```
function operation(arr,n,k){
    let ans=[]
    let count=0
    for(let i=0;i<n;i++){
      if(count<2){
            if(arr[i]<=k)  ans.push(arr[i])
            else           count++;
       }
       else break;
    }
    console.log(ans.length)
}

```
