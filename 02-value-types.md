# Tipos de valores

## Enteros (Integers)

Los números enteros pueden ser representados en los siguientes formatos:

- Decimal (1234567890)
- Hexadecimal (F69B5)
- Octal (0o675))
- Binario (0b1001)

No hay un límite de dígitos para los números enteros.

## Flotantes (Floats)

Los números flotantes son escritos con un **.** y un mínimo de un dígito después del **.**, también puedes utilizar notación científica en estos:

- 1.0
- 97.3245
- 3178321.56
- 12.93e10
- 12.93e-5

## Booleanos (Booleans)

Elixir soporta dos tipos de booleanos `true` y `false`.

```elixir
iex> true
true
iex> false
false
iex> true == false
false
```

Además cuenta con varias funciones para comprobar el tipo de valor.

```elixir
iex> is_boolean(true)
true
iex> is_boolean(32)
false
```

## Átomos (Atoms)

Los átomos son constantes, en los cuáles su nombre es su valor, en algunos lenguajes son conocidos como "símbolos". Podemos utilizar la función `is_boolean/1` para comprobar si es un átomo.

```elixir
iex> :nombre
:nombre
```

```elixir
iex> :nombre == :apellido
false
```

Los booleanos `true` y `false` son átomos

```elixir
iex> :true == true
true
iex> is_atom(true)
true
iex> is_boolean(:false)
true
```

## Cadenas (Strings)

Los strings en elixir son definidos por un par de comillas dobles `" "` y son codificados en UTF-8.

```elixir
iex> "Hola"
```

Elixir también soporta interpolación de strings

```elixir
iex> "Hola #{:mundo}"
"Hola mundo"
```

Puedes imprimir un string utilizando la función `IO.puts/1` del módulo `IO`.

```elixir
iex> IO.puts "Hola mundo!"
Hola mundo!
:ok
```

## Funciones anónimas (Anonymous functions)

Las funciones anónimas son caracterizadas por utilizar `fn`.

```elixir
iex> suma = fn a, b -> a + b end
Output
iex> is_function(suma)
true
iex> is_function(suma, 2)
true
iex> is_function(suma, 1)
false
iex> suma.(1, 2)
3
```

Notése el **.** (punto) entre la función y sus parámetros, las funciones anónimas requieren de este punto para ser utilizadas.

## Listas (Lists)

Elixir utiliza corchetes `[ ]` para crear listas, que pueden contener cualquier tipo de valor.

```elixir
iex> [1, 2, true, 3]
[1, 2, true, 3]
iex> length [1, 2, 3]
3
```

Dos listas pueden ser concatenadas usando los operadores `++/2` y `--/2`:

```elixir
iex> [1, 2, 3] ++ [4, 5, 6]
[1, 2, 3, 4, 5, 6]
iex> [1, true, 2, false, 3, true] -- [true, false]
[1, 2, 3, true]
```

## Tuples

Elixir usa llaves para definir tuples, al igual que las listas, los tuples pueden contener cualquier tipo de valor.

```elixir
iex> {:ok, "hola"}
{:ok, "hola"}
iex> tuple_size {:ok, "hola"}
2
```

También puedes consultar por un elemento de un tuple:

```elixir
iex> elem(tuple, 1)
"hola"
```

Para añadir un elemento a un tuple existente, puedes utilizar `put_elem/3`.

```elixir
iex> tuple = {:ok, "hola"}
{:ok, "hola"}
iex> put_elem(tuple, 1, "mundo")
{:ok, "mundo"}
iex> tuple
{:ok, "hola"}
```

## Mapas (Maps)

Los mapas son una colección de pares de key/value, la estructura de un mapa es la siguiente

```elixir
%{key => value, key => value}
```

Ó

```elixir
%{key: value, key: value}
```

La diferencia, es que al usar la segunda retornaremos atoms.

Con lo anterior dicho, podemos definir un mapa así

```elixir
iex> paises = %{"COL" => "Colombia", "ESP" => "España", "MEX" => "México"}
%{"COL" => "Colombia", "ESP" => "España", "MEX" => "México"}
```

Ó

```elixir
iex> paises = %{US: "Estados Unidos", UK: "Reino Unido"}
%{US: "Estados Unidos", UK: "Reino Unido"}
```

Podemos acceder al mapa de la siguiente manera si usamos el primer método

```elixir
iex> paises["COL"]
"Colombia"
```

Si usas el segundo método, debes utilizar un atom en su lugar

```elixir
iex> paises[:US]
"Estados Unidos"
```

Para más información, se recomienda visitar [Basic Types](http://elixir-lang.org/getting-started/basic-types.html).
