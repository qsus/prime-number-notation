# prime-number-notation
Idea how we could store numbers in computers using prime numbers.
## Idea
Computers store numbers in binary - that means our base 10 numbers have to be converted to ones and zeroes. For example 9 in decimal would be written as 1001 in binary. Converting it back to decimal is easy: 1×2³+0×2²+0×2¹+1×2⁰=8+1=9. For each bit n, we're basically multiplying it's value with 2^n and adding it to the total.
But what if we instead imagined numbers as a product of primes? That would mean that 1001 is 7~~×5×3~~×2=14. So for each bit, we are either multiplying or not multiplying the total by nth prime.
## Conversion and examples
|nth bit  |  n| 6| 5|4|3|2|1|
|---------|---|--|--|-|-|-|-|
|bit value|...|13|11|7|5|3|2|
|example 1|   | 0| 0|1|0|1|1|
|example 2|   | 1| 0|0|1|0|0|   
|example 3|   | 0| 0|0|0|1|1|
1. 7×3×2=42
2. 13×5=65
3. 3×2=6

As you can see, converting from prime number notation is simple, but converting it into prime number notation requires factorisation.
## Advantages
Unknown yet.
## Problems and details
### Unability to express negative numbers
#### The obvious solution
Suffix the number with -1 bit. Numbers ending with 1 are negative, numbers ending with 0 are positive.
#### Extending prime numbers to negative numbers
Too complicated, I didn't research it yet. And it might end up being a total nonsense.
### Unability to express numbers 0 and 1
What does 0000 mean? Is is 1 or 0? I would argue it's 1, for a similar reason why 0! is 1. So how do we define the other number? Here are the solutions I could think of:
#### 1. Extending prime numbers so that they include one
#### 2. Extending prime numbers so that they include zero
|Decimal|Without solution|First solution|Second solution|
|------:|---------------:|-------------:|--------------:|
|      2|             001|          0011|           0010|
|      1|undefined or 000|          0001|           0000|
|      0|undefined or 000|          xxx0|           xxx1|

(x means any boolean value)

TODO: add description to this table. Below is a text I wrote, but didn't finish, so please ignore that.
_Other solution would be that the last bit isn't multiplying by one, but by zero.
For example 6 would be written as 111=3×2×1. 0 would be written as 0, or as 10, 10110, ... it could be written in infinitely many ways and all numbers would be 0, as long as the last bit is 0. Not only that, it would break the initial assumption that 0000 is 1. And the third problem is that all other numbers now have to have one extra useless bit.
Could be solved by adding two bits at the end. One would be multiplying by one (basically redefining prime numbers so they include one). In that case every number would look like xxx1x (I'll talk about the last bit in the next paragraph), except for number_

End of text to be ignored.
### How do I write 4?
Oh no, I've realised this dumb mistake after writing 39 lines of markdown... Never mind, I'll finish it and think about this problem later. I'm tired.

Note: all numbers are written in decimal, unless noted otherwise.
