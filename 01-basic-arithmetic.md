# Aritmética básica

Elixir permite realizar las operaciones aritméticas básicas

```elixir
iex> 1 + 2
3
iex> 5 - 4
1
iex> 5 * 5
25
iex> 25 / 5
5.0
```
*Al utilizar `/` Elixir siempre retornará un decimal*

De igual manera puedes hacer uso de `div` para obtener un resultado en número entero

```elixir
iex> div(25, 5)
5
iex> div 25, 5
5
```

También podemos utilizar `rem` para obtener el residuo de una división

```elixir
iex> rem 10 / 3
1
```

Puedes utilizar múltiples expresiones al añadir `;` y IEX retornará el resultado de la última operación

```elixir
iex> 2 + 3; 5 + 5
10
```
