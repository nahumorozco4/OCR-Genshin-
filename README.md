# Genshin Impact Tracker v6

PWA instalable y offline para controlar ahorro, protogemas, deseos, pity y progreso hacia una meta.

## Cambios principales
- Los ingresos nuevos pueden **sumarse automáticamente al saldo** y entrar al historial en una sola operación.
- Botón **“📦 Ya existente”** para registrar algo que ya estaba incluido en el saldo sin volver a sumarlo.
- Acceso rápido a **Diarias de hoy (+60 💎)**; evita registrarlas dos veces el mismo día.
- “Registrar saldo actual” funciona como sincronización: calcula la diferencia y la guarda como movimiento.
- Ajustes negativos de saldo quedan registrados en el historial.
- Deshacer revierte el último movimiento positivo y marca como no aplicado el ingreso asociado cuando corresponde.
- Importación validada y compatible con los datos de la versión anterior.
- Service Worker versionado con limpieza de cachés antiguas.
- Sin dependencias de fuentes externas para que la interfaz sea realmente usable offline.
- Manifest preparado para instalación como aplicación independiente.

## Estructura
- index.html
- app.js
- styles.css
- manifest.json
- service-worker.js
- icons/icon-192.png
- icons/icon-512.png

## Regla de uso
1. **Registrar ingreso** = acabo de conseguir esas protogemas → se suman al saldo.
2. **Ya existente** = esas protogemas ya están en mi saldo → solo se crea el registro.
3. **Registrar saldo actual** = quiero que el tracker coincida exactamente con el saldo que muestra el juego.

Los datos se guardan localmente en el dispositivo mediante `localStorage`.
