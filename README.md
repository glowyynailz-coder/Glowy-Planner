# Glowy Planner ♡ — versión 0.1

Web-app **personal y gratuita**, sin cuenta del instituto, con interfaz rosa pastel. Funciona con archivos HTML, CSS y JavaScript sin servicios de pago ni dependencias.

## Qué funciona ya
- Inicio con saldo calculado, ingresos y gastos mensuales, tareas y accesos.
- Agenda mensual: eventos, tareas fechadas, suscripciones previstas.
- Tareas: añadir, marcar completadas y borrar.
- Finanzas: gastos/ingresos con categoría, subcategoría, cuenta y método; transferencias entre cuentas; presupuesto por categoría; suscripciones previstas; saldos.
- Goals: nueve objetivos precargados, cantidades y progresos editables.
- Wellness: hábitos diarios marcables.
- Study Space: cursos/formaciones y eventos de Estudios conectados con Agenda.
- My Space: notas personales.
- Copias de seguridad: exportar/importar JSON, confirmar antes de reemplazar, borrar datos manualmente.
- Manifest e iconos PWA y service worker para que, tras publicarla por HTTPS y cargarla, funcione también sin conexión en condiciones normales.

## Limitaciones actuales
- Los datos se guardan **solo en el almacenamiento local del navegador**. No hay sincronización, registro de usuarios ni cifrado de los datos. El modo privado o borrar datos del sitio puede hacer que se pierdan. Guarda copias frecuentes.
- Las suscripciones son **previsiones**, no se cargan automáticamente como movimientos reales para evitar contabilizar cargos no confirmados.
- No hay notificaciones push, integración bancaria, archivos adjuntos, calendario arrastrable, vision board ni todas las funciones avanzadas de los diseños de referencia.
- Para privacidad, no subas archivos de datos JSON ni información personal al repositorio público.
- No constituye asesoramiento financiero.

## Probarla en el ordenador
En esta carpeta, con Python instalado:

```bash
python -m http.server 8000
```

Abrir `http://localhost:8000` en tu navegador. También puedes abrir `index.html` directamente para probar gran parte de la interfaz, pero la instalación offline requiere HTTPS o localhost.

## Publicarla gratis con GitHub Pages
1. Crea una cuenta personal de GitHub (no la del instituto).
2. Crea un repositorio **público**, por ejemplo `glowy-planner`. No subas copias de seguridad.
3. Sube el contenido de esta carpeta a la raíz del repositorio (NO la carpeta contenedora).
4. En **Settings → Pages**, selecciona **Deploy from a branch**, rama **main**, carpeta **/(root)** y guarda.
5. Espera a que aparezca el enlace `https://TU-USUARIO.github.io/glowy-planner/`.
6. Ábrelo en Safari en tu iPhone. Pulsa **Compartir → Añadir a pantalla de inicio** y, si aparece, activa **Abrir como app**.

GitHub Pages gratis requiere un repositorio público. Esto hace público el código, no los datos que escribas dentro de la app, que solo quedan en el dispositivo. **No introduce protección por contraseña**. No pongas datos personales en el código ni en GitHub.

## Trabajar con Codex
1. Entra con tu **cuenta personal de ChatGPT** en la app o entorno de Codex que tengas disponible.
2. Abre la carpeta `glowy-planner` o el repositorio Git asociado.
3. Prueba una tarea concreta, por ejemplo:

> Revisa esta PWA vanilla de Glowy Planner. Añade una pantalla de balance anual que agrupe transacciones por meses sin alterar el almacenamiento actual, con pruebas de los cálculos y manteniendo el estilo rosa pastel.

4. Revisa cambios y pruebas antes de publicar.

## Próximas iteraciones recomendadas
1. Pruebas automáticas de los cálculos de saldos y presupuestos.
2. Calendario semanal y diario con recurrencias verificadas.
3. Registro detallado de materias, notas ponderadas y prácticas.
4. Gráficos anuales y gastos hormiga.
5. Acceso opcional con contraseña local y cifrado de exportaciones (requiere diseño cuidadoso y revisión de seguridad).

## Importante al actualizar
El service worker usa un nombre de caché (`glowy-v1`) en `sw.js`. Cuando cambies código, cambia ese nombre por `glowy-v2`, etc., para forzar que se refresquen los archivos offline.
