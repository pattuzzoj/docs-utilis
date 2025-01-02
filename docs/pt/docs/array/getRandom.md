# getRandom

```typescript
function getRandom<T>(arr: T[]): T {
  return arr[Math.floor(Math.random() * arr.length)];
}
```

A função `getRandom` retorna um elemento aleatório do array.

## Assinatura

```typescript
function getRandom<T>(arr: T[]): T;
```

### Parâmetros

- **`arr`** (`T[]`): O array do qual um elemento aleatório será selecionado.

### Retorno

- **`T`**: Um elemento aleatório do array.

## Exemplos

```typescript
console.log(getRandom([1, 2, 3, 4, 5])); // Pode retornar qualquer elemento do array
```

## Notas

- A função usa `Math.random` e `Math.floor` para selecionar um índice aleatório do array.

## Referências

- [Math.random() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
- [Math.floor() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)