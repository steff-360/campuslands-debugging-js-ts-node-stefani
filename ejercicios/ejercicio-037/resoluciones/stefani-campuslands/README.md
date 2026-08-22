# Resolucion Ejercicio 037

## Error encontrado
Comparacion de tipos en GET /items/:id, status HTTP incorrecto en not found y en POST.

## Causa raiz
1. req.params.id es string pero ids son numeros, === nunca encontraba coincidencia.
2. Retornaba 200 en vez de 404 cuando item no existia.
3. POST retornaba 200 en vez de 201.

## Cambio aplicado
1. Agrego Number(req.params.id) para convertir parametro.
2. Cambio a res.status(404) en not found.
3. Cambio a res.status(201) en creacion.

## Comando de validacion
npm test -- ejercicios/ejercicio-037/tests/tournaments.api.test.js

## Resultado
Tests pasan correctamente.