# Make the Deadfish Swim (6 kyu)
## Link
https://www.codewars.com/kata/51e0007c1f9378fa810002a9/typescript

## Description
Write a simple parser that will parse and run Deadfish.

Deadfish has 4 commands, each 1 character long:

- `i` increments the value (initially `0`)
- `d` decrements the value
- `s` squares the value
- `o` outputs the value into the return array
Invalid characters should be ignored.

```typescript
parse("iiisdoso") => [8, 64]
```

## Solution
```typescript
export function parse(data: string): number[] {
  const result: number[] = [];
  let value = 0;

  for (const cmd of data.split('')) {
    if (cmd == 'i') value += 1;
    if (cmd == 'd') value -= 1;
    if (cmd == 's') value *= value;
    if (cmd == 'o') result.push(value);
  }

  return result;
}
```