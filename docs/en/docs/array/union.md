# union

The `union` function returns a new array containing the unique elements from all the provided arrays. It is useful for combining multiple arrays into one without duplicates.

## Syntax

```typescript
function union<T>(...arrs: T[][]): T[];
```

### Parameters

| Name   | Type     | Description                                              |
|--------|----------|--------------------------------------------------------|
| `arrs` | `T[][]`  | The arrays to be combined.                               |

### Return

| Type   | Description                                              |
|--------|--------------------------------------------------------|
| `T[]`  | A new array containing the unique elements from all the provided arrays. |

## Examples

```typescript
console.log(union([1, 2], [2, 3])); // [1, 2, 3]
console.log(union([1, 2], [3, 4], [4, 5])); // [1, 2, 3, 4, 5]
```

## Notes

- The order of elements in the returned array is determined by the order of their first appearance in the input arrays.
- [unique](./unique.md): The `unique` function is used to ensure the elements in the final array are unique, removing duplicates from the combined arrays.

## Source Code

::: code-group
```typescript
import unique from "./unique";

function union<T>(...arrs: T[][]): T[] {
  return unique(
    arrs.reduce((unionArr, arr) => {
      unionArr = [...unionArr, ...arr];
      return unionArr;
    }, [])
  );
}
```
```javascript
import unique from "./unique";

function union(...arrs) {
  return unique(
    arrs.reduce((unionArr, arr) => {
      unionArr = [...unionArr, ...arr];
      return unionArr;
    }, [])
  );
}
```
:::

## References

- [Array.prototype.reduce() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)