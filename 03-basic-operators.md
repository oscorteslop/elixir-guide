# Operadores básicos

Es posible utilizar `++` y `--` para manipular listas:

```elixir
iex> [1,2,3] ++ [4,5,6]
[1,2,3,4,5,6]
iex> [1,2,3] -- [2]
[1,3]
```

La concatenación de strings se realiza con `<>`

```elixir
iex> "Hola " <> "mundo"
"Hola mundo"
```

Elixir provee tres operadores para booleanos: `or`, `and` y `not`. Estos esperan un booleano como primer argumento.

```elixir
iex> false and false
false
iex> true and true
true
iex> false or is_atom(:ok)
```

Además de estos operadores, elixir también provee `||`, `&&` y `!` que aceptan argumentos de cualquier tipo.

```elixir
# or
iex> 1 || true
1

# and
iex> true && 17
17

# !
iex> !true
false
```

Para realizar comparaciones, podemos hacer uso de `===`, `!=`, `<`, `>`, `<=`, `>=`, `==` y `!==`.

```elixir
iex> 1 == 1
true
iex> 1 === 1.0
false
```
