# hoy-datos

Datos públicos de **Hoy · AvilesIA** (https://hoy.avilesia.es). Los escribe un flujo de n8n en el VPS de AvilesIA; la web los lee a través de su función `api/datos.js`, que los valida (esquema y fecha, falla cerrado) antes de servirlos.

| Fichero | Qué es | Cuándo se actualiza | Fuente |
|---|---|---|---|
| `luz.json` | PVPC 2.0TD de hoy y, desde ~20:15, de mañana (€/kWh por hora) | 00:10 y 20:35 (hora de Madrid) | Red Eléctrica (REE), apidatos |
| `farmacias.json` | Guardias de hoy de los concejos de Asturias | 6 veces al día: 00:20, 08:20, 10:20, 13:20, 17:20 y 21:20 (hora de Madrid) | Colegio Oficial de Farmacéuticos de Asturias |
| `gasolina.json` | Media de gasolina 95 y gasóleo A a 10 km y las 5 más baratas, por municipio | a diario, 06:40 (hora de Madrid) | Geoportal de carburantes (Ministerio para la Transición Ecológica) |

No edites a mano: lo sobrescribe el flujo. Un dato que no es de hoy no se sube (se queda el último bueno con su fecha y la web avisa).

## Reutilización

Estos ficheros se publican para que funcione la web de Hoy. Si los reutilizas:

- **Cita la fuente original** que lleva cada fichero en `fuente` y respeta sus condiciones: REE (condiciones de uso de apidatos), Colegio Oficial de Farmacéuticos de Asturias (las guardias son suyas; consúltalo antes de reutilizarlas) y Ministerio para la Transición Ecológica y el Reto Demográfico (Geoportal de carburantes). Las coordenadas de las farmacias de Avilés vienen de CartoCiudad (IGN-CNIG), CC BY 4.0 scne.es.
- **Sin garantía:** pueden estar incompletos o desfasados. Mira siempre la fecha de cada fichero. Para urgencias, llama al 112; antes de ir a una farmacia, llama.
- No hay datos personales más allá de los nombres, direcciones y teléfonos públicos de las farmacias, tal y como los publica el COF.
