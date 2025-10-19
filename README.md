# Tarea 1 — Laboratorio de Lenguajes de Programación I
Práctica de Haskell

###### Alumno: Kevin Briceño
###### Carnet: 15-11661

### Estructura del Proyecto

```
Tarea1/
├── src/
│   ├── Main.hs
│   └── Tarea1.hs
├── test/
│   └── Test.hs
├─ package.yaml
├─ stack.yaml
└─ Tarea_l_Laboratorio_de_Lenguajes_de_programación.pdf
```

### 📘 Analisis de las funciones de la Tarea 1:
Contiene las implementaciones solicitadas en la Tarea 1:

- esPalindromo :: String -> Bool
  - Determina si la cadena es palíndromo usando recursión explícita.

- productoParesRec :: [Integer] -> Integer
  - Calcula el producto de los números pares de una lista de forma puramente recursiva. Devuelve 1 si no hay pares.

- parsearCondicional :: [String] -> [Either String Int]
  - Convierte cadenas a enteros con manejo seguro de errores (readMaybe). Devuelve Right Int si parsea o Left String en mayúsculas si falla.

- sumaAcumuladaCondicional :: Float -> [Float] -> Float
  - Filtra los valores mayores al umbral y calcula la suma usando fold.

- coordenadasImpares :: Int -> [(Int, Int)]
  - Genera todos los pares (x, y) con x,y ∈ [1..N] tales que x + y es impar. Implementada con comprensión de listas.

- descomponerListaSegura :: [a] -> Maybe (a, [a])
  - Devuelve Nothing si la lista está vacía o Just (head, tail) si tiene elementos.

### 🧩Dependencias

- `GHC >= 9.0`
- `Stack o Cabal` como gestor de proyectos.
- `base >= 4.7 && < 5`
- `HUnit` para pruebas unitarias.

### ⚙️Compilación y Ejecución de Tests

#### A — Usando Stack
Asegúrate de tener HUnit incluido en test-depends dentro del package.yaml.

```
stack setup
stack build
stack test
```

#### B — Usando GHC directamente
Desde la raíz del proyecto:
```
ghc --make src/Tarea1.hs test/Test.hs
.\test\Test.exe
```
Salida esperada:
```
Cases: 6  Tried: 6  Errors: 0  Failures: 0
```
