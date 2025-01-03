# isIterable

A função `isIterable` verifica se o objeto é iterável.

## Sintaxe

```typescript
function isIterable(obj: any): boolean;
```

### Parâmetros

| Nome  | Tipo    | Descrição                                          |
|-------|---------|----------------------------------------------------|
| `obj` | `any`   | O objeto a ser verificado.                         |

### Retorno

| Tipo    | Descrição                                           |
|---------|-----------------------------------------------------|
| `boolean` | `true` se o objeto for iterável, caso contrário `false`. |

## Exemplos

```typescript
console.log(isIterable([1, 2, 3])); // true
console.log(isIterable(123));       // false
```

## Notas

- A função verifica se o objeto possui a propriedade `Symbol.iterator`.

## Código Fonte

::: code-group
```typescript
function isIterable(obj: any): boolean {
  return obj != null && typeof obj[Symbol.iterator] === 'function';
}
```
```javascript
function isIterable(obj) {
  return obj != null && typeof obj[Symbol.iterator] === 'function';
}
```
:::

## Referências

- [Symbol.iterator - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator)