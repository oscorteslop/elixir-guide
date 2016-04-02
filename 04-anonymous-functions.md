# Funciones anónimas

Elixir es un lenguage funcional, no creo que te sorprendas si te digo que cuenta con funciones.

Las funciones anónimas se definen utilizando `fn` y son invocadas utilizando un punto `.`

Podriamos definir una función que tome un parametro (nombre)

```elixir
iex>bienvenida = fn (nombre) -> IO.puts "Hola #{nombre}" end
iex>bienvenida.("Andres")
Hola Andres
```
