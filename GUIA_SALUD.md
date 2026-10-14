# NutriDía · Conectar con Apple Salud (Garmin, Mi Band, Apple Watch)

Apple no permite que una web lea Salud directamente. Se hace con dos atajos de la app Atajos. Solo hay que crearlos una vez.
Los nombres de las acciones pueden variar ligeramente según la versión de iOS.

## 0. Que tu reloj escriba en Salud
- **Garmin Connect:** Más › Ajustes › Apps conectadas › Apple Salud, y activa todo.
- **Mi Fitness / Zepp Life (Mi Band):** Perfil › Añadir cuentas › Apple Salud.
- Comprueba en **Salud › Compartir** que escriben Energía activa, Pasos y Peso.

## 1. Atajo «NutriDía desde Salud» (Salud › NutriDía)
El nombre tiene que ser exacto.
1. **Buscar muestras de salud:** Tipo = Energía activa, Fecha de inicio = hoy, Agrupar por = Día. Después **Obtener detalles de muestras de salud › Valor**. Renombra el resultado como «Activas».
2. Repite lo mismo para Pasos («Pasos») y, si quieres, Energía en reposo («Reposo»).
3. **Peso:** Buscar muestras de salud con Tipo = Peso, ordenadas por Fecha de inicio (más reciente primero), Límite 1. Después Obtener detalles › Valor («Peso»).
4. **Formatear fecha:** Fecha actual, formato personalizado `yyyy-MM-dd`.
5. **Texto:** `nutridia:fecha=[Fecha];activas=[Activas];reposo=[Reposo];pasos=[Pasos];peso=[Peso]`
6. **Copiar al portapapeles.**
   - Si usas NutriDía en Safari y no desde la pantalla de inicio, puedes usar en su lugar **Abrir URL** con `https://TU-WEB/?fecha=[Fecha]&activas=[Activas]&reposo=[Reposo]&pasos=[Pasos]&peso=[Peso]`.

**Uso:** en Hoy › tarjeta Actividad, pulsa **Obtener**. Cuando termine el atajo, vuelve a NutriDía y pulsa **Pegar datos**.
Opcional: crea una automatización diaria (por ejemplo a las 22:00) que ejecute el atajo.

## 2. Atajo «NutriDía a Salud» (NutriDía › Salud)
1. En los ajustes del atajo, activa que reciba **Texto** como entrada.
2. **Obtener diccionario de** Entrada del atajo.
3. Toma la clave «fecha» y conviértela en fecha. Después **Ajustar fecha** + 21 horas.
4. Para cada clave, **Obtener valor de diccionario** + **Registrar muestra de salud** con esa fecha:

| Clave | Tipo en Salud |
|---|---|
| kcal | Energía de la dieta |
| proteinas | Proteína |
| hidratos | Carbohidratos |
| grasas | Grasa total |
| fibra* | Fibra |
| azucares* | Azúcar |
| saturadas* | Grasa saturada |
| sodio_mg* | Sodio (mg) |

\* Estas claves solo llegan si tus alimentos informan ese dato. Mete esas acciones dentro de un **Si** «tiene cualquier valor».

**Uso:** en NutriDía, menú ⋯ del día › **Enviar nutrición a Salud**. Envíalo una vez por día: si lo envías dos veces, Salud lo suma dos veces. NutriDía te avisa si ya lo enviaste.

## Probar sin atajos
Copia `nutridia:activas=420;pasos=9800;peso=77,4` y usa ⋯ › **Pegar datos de Salud**.
