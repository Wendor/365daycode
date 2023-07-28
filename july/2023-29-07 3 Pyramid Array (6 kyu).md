# Pyramid Array (6 kyu)
## Link
https://www.codewars.com/kata/515f51d438015969f7000013/train/typescript

## Description
Write a function that when given a number >= 0, returns an Array of ascending length subarrays.

```
pyramid(0) => [ ]
pyramid(1) => [ [1] ]
pyramid(2) => [ [1], [1, 1] ]
pyramid(3) => [ [1], [1, 1], [1, 1, 1] ]
```
Note: the subarrays should be filled with `1`s


## Solution
```typescript
export function pyramid(n: number) {
  const result: number[][] = [];
  while (result.length < n) {
    result.push(Array(result.length + 1).fill(1));
  }
  return result;
}
```