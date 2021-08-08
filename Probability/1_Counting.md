# Counting

## Rule Of Sum

The rule of sum is a basic counting approach in combinatorics. A basic statement of the rule is that if there are $n$ choices for one action and $m$ choices for another action, and the two actions cannot be done at the same time, then there are $n+m$ ways to choose one of these actions.

The rule of sum only applies to choices that are mutually exclusive, meaning that only one of the choices can be picked. To determine when to use the rule of sum (as opposed to the rule of product), try to rephrase the question. If the question can be rephrased with the word "or," this usually indicates that the rule of sum applies.

> EXAMPLE  
> Mary is wearing her lucky shirt today, and she has to choose among 3 red skirts and 4 blue skirts to wear with the shirt. How many different outfit choices of one skirt does she have for the day?
>
> Since Mary can wear one of the 3 red skirts or one of the 4 blue skirts, the choices are mutually exclusive and the rule of sum applies. This gives a total of 3 + 4 = 7 different outfit choices.

## Counting Integers in a Range

 In a closed interval $[a,b]$, the number of integers is $b-a+1$.  
> Example: $[1,10]=10-1+1=10$

 In an open interval $(a, b)$ the number of integers is $b-a-1$.  
> Example: $(1,10)=10-1-1=8$

 In a half-open interval $[a, b)$ or $(a,b]$, the number of integers is $b-a$.  
> Example: $(1,10] or [1,10) = 10-1=9$

## Rule Of Product

The rule of product states that if there are $n$ ways of doing something, and $m$ ways of doing another thing after that, then there are $n \times m$ ways to perform both of these actions. In other words, when choosing an option for nn and an option for mm, there are $n \times m$ different ways to do both actions.

> EXAMPLE 1 (Basic Example)
> There are 8 daily newspapers and 5 weekly magazines published in Chicago. If Colin wants to subscribe to exactly one daily newspaper and one weekly magazine, how many different choices does he have?  
> Colin has $8 \times 5=40$ choices.

> EXAMPLE 2​  
> Calvin wants to go to Milwaukee. He can choose from 3 bus services or 2 train services to head from home to downtown Chicago. From there, he can choose from 2 bus services or 3 train services to head to Milwaukee. How many ways are there for Calvin to get to Milwaukee?  
> He has $3 + 2=5$ ways to get to downtown Chicago. [Rule of sum](#rule-of-sum)  
> From there, he has $2+3=5$ ways to get to Milwaukee. [Rule of sum](#rule-of-sum)  
> Hence, he has $5 \times 5=25$ ways to get to Milwaukee in total. [Rule of product](#rule-of-product)

## Permutations

In combinatorics, a permutation is an ordering of a list of objects. For example, arranging four people in a line is equivalent to finding permutations of four objects. More abstractly, each of the following is a permutation of the letters a, b, c,a,b,c, and d:

$$
\begin{aligned}
→ \ & a, b, c, d\\
→ \ & a, c, d, b\\
→ \ & b, d, a, c\\
→ \ & d, c, b, a\\
→ \ & c, a, d, b.
\end{aligned}
$$

> Given a list of $n$ distinct objects, how many different permutations of the objects are there?
> Since each permutation is an ordering, start with an empty ordering which consists of $n$ positions in a line to be filled by the n objects. There are $n$ choices for which object to place in the first position. After the first object is placed, there are $n-1$ remaining objects, so there are $n-1$ choices for which object to place in the second position. Repeating this argument, there are $n-2$ choices for the third position, $n-3$ choices for the fourth position, and so on. For the $n^{th}$ position, the number of choices is $n - (n-1)= 1$. Then the rule of product implies the total number of orderings is
>$$n \times (n-1) \times (n-2) \times (n-3) \times \cdots \times 1 = n!$$
>For a positive integer $n$, the notation $n!$ denotes the factorial of n and refers to the product of all positive integers from $1$ to $n$. Note that $0!$ is the empty product and is defined to be $1$.

### Permutations with Repetition

The number of permutations of $n$ objects with $n_1$ identical objects of type 1, $n_2$ identical objects of type 2,..., and $n_k$ identical objects of type k is
$$\frac{n!}{n_1!n_2!...n_k!}$$

>EXAMPLE
>How many ways can the letters in the name RAMONA be arranged?
>Observe that the letter A appears twice and all other letters appear once in the word. If we treat the A's as distinct from each other (say $A_1$ and $A_2$), then there are $6! = 720$ ways to rearrange the letters. However, since the letters are the same, we have to divide by $2!$ to obtain $\frac{720}{2!}=360$ ways.

### Permutations With Restriction

Given n distinct objects, the number of different ways to place $k$ of them into ordering is
$$P_k^n=n(n-1)(n-2)...(n-k+1)=\frac{n!}{(n-k)!}$$
This is also known as $k$-permutations of $n$

> EXAMPLE
> Lisa has 13 different ornaments and wants to put 4 ornaments on her mantle. In how many ways is this possible?
>Using the product rule, Lisa has 13 choices for which ornament to put in the first position, 12 for the second position, 11 for the third position, and 10 for the fourth position. So the total number of choices she has is $13 \times 12 \times 11 \times 10$. Using the factorial notation, the total number of choices is $\frac{13!}{9!}$.

## Combinations

A combination is a way of choosing elements from a set in which order does not matter

Consider the following example: Lisa has $12$ different ornaments and she wants to give $5$ ornaments to her mom as a birthday gift (the order of the gifts does not matter). How many ways can she do this?

We can think of Lisa giving her mom a first ornament, a second ornament, a third ornament, etc. This can be done in $\frac{12!}{7!}$ ways. However, Lisa’s mom is receiving all five ornaments at once, so the order Lisa decides on the ornaments does not matter. There are $5!$ reorderings of the chosen ornaments, implying the total number of ways for Lisa to give her mom an unordered set of $5$ ornaments is $\frac{12!}{7!5!}$.

Notice that in the answer, the factorials in the denominator sum to the value in the numerator. This is not a coincidence. In general, the number of ways to pick $k$ unordered elements from an $n$ element set is $\frac{n!}{k!(n-k)!}$.
This is a binomial coefficient.

$$\binom{n}{k}=\frac{n!}{k!(n-k)!}$$

>EXAMPLE 1 Basic
>Out of $7$ consonants and $4$ vowels, how many words of $3$ consonants and $2$ vowels can be formed?
>The number of ways of selecting $3$ consonants out of $7$ and $2$ vowels out of $4$ is ${7\choose3}\times{4\choose2} = 210$.
>Therefore, the number of groups each containing $3$ consonants and $2$ vowels is $210$. Since each group contains $5$ letters, which can be arranged amongst themselves in $5! = 120$ ways, the required number of words is $210 \times 120 = 25200$.  

>EXAMPLE 2 Intermediate
>We are trying to divide $5$ European countries and $5$ African countries into $5$ groups of $2$ each. How many ways are there to do this under the restriction that at least one group must have only European countries?
>The number of ways to divide $5+5=105+5=10$ countries into $5$ groups of $2$ each is as follows:
>$$\frac{{10\choose2} \times {8\choose2} \times {6\choose2} \times {4\choose2} \times {2\choose2}}{5 !} =\frac{ 45 \times 28 \times 15 \times 6 \times 1}{120}=945$$
>Since it is required that at least one group must have only European countries, we need to subtract from $(1)$ the number of possible groupings where all $5$ groups have $1$ European country and $1$ African country each. This is equivalent to the number of ways to match each of the $5$ European countries with one African country:
$5! = 5 \times 4 \times 3 \times 2 \times 1=120.  (2)$
Therefore, taking $(1)-(2)$ gives our answer $945-120=825$.

​
<!-- TODO: Add a complex example -->