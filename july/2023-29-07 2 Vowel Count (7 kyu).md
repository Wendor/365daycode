# Vowel Count 7 kyu)
## Link
https://www.codewars.com/kata/54ff3102c1bad923760001f3/train/typescript

## Description
Return the number (count) of vowels in the given string.

We will consider `a`, `e`, `i`, `o`, `u` as vowels for this Kata (but not `y`).

The input string will only consist of lower case letters and/or spaces.


## Solution
```typescript
export class Kata {
  static getCount(str: string): number {
    return str.match(/[aeiou]/g)?.length ?? 0;
  }
}
```