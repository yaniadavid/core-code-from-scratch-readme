<h1 align="center">Week 6</h1>
Learn about classes, instances, inheritance and data type with Typescript

# Monday, May 16th
## [Square(n) Sum](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript "Square(n) Sum")
Complete the square sum function so that it squares each number passed into it and then sums the results together.
```typescript
export function squareSum(numbers: number[]): number {
    return numbers.reduce(
      (prev: number, curr: number) => prev + Math.pow(curr,2), 0
    );
}
```

