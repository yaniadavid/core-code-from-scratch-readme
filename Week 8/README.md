<h1 align="center">Week 8</h1>

Lear about interfaces, data modifiers and function types, along with how to interact with the console using typescript

# Wednesday, June 1st
## [Make the Deadfish Swim](https://www.codewars.com/kata/51e0007c1f9378fa810002a9/train/typescript "Make the Deadfish Swim")
Write a simple parser that will parse and run Deadfish. <br>
Deadfish has 4 commands, each 1 character long: <br>
i increments the value (initially 0) <br>
d decrements the value <br>
s squares the value <br>
o outputs the value into the return array <br>
Invalid characters should be ignored. <br>

```typescript
export function parse(data: string): number[] {
  let value: number = 0;
  let result: number[] = [];
  for(let i = 0; i < data.length; i++){
    if(data[i] === 'i') value++;
    if(data[i] === 'd') value--;
    if(data[i] === 's') value = Math.pow(value,2);
    if(data[i] === 'o') result.push(value);
  }
  return result;
}
```

# Thursday, June 2nd
## Generics
We have just learn about generics, an we where creating our own implementation for the Linkedlist structure, but it is incomplete, you task is to finish the missing methods.

- addFirst: Adds a new node at the start of the structure
- removeLast: Removes the last node of the structure

Solution <br>
addFirst 
```typescript
 public addFirst(value: T) {
    if (this.head === null) {
      this.add(value);
    } else {
      let node = new Node(value);
      node.next = this.head;
      this.head = node;
      this.length++;
    }
  }
```

RemoveLast
```typescript
  public removeLast(): void {
    if (this.head !== null) {
      let node = this.head;
      let previous: Node<T> = node;
      while (node.next !== null) {
        previous = node;
        node = node.next;
      }
      previous.next = null;
      this.length--;
    }
  }
```
