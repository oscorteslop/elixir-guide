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
```

Puedes imprimir un string utilizando la función `IO.puts/1` del módulo `IO`.

```elixir
iex> IO.puts "Hola mundo!"
Hola mundo!
:ok
```

Para más información, se recomienda visitar [Basic Types](http://elixir-lang.org/getting-started/basic-types.html).
