# Resolucion Ejercicio 027

## Error encontrado
calcularPromedio dividia entre total de registros en vez de solo activos. obtenerMejor devolvia el menor puntaje.

## Causa raiz
1. Dividia entre registros.length (todos) en vez de activos.length (solo activos).
2. Sort ascendente a.puntos - b.puntos tomando [0] devolvia el menor.

## Cambio aplicado
1. Cambio a total / activos.length.
2. Sort cambiado a b.puntos - a.puntos.

## Comando de validacion
npm test -- ejercicios/ejercicio-027/tests/bpm-validator.test.ts

## Resultado
Tests pasan correctamente.