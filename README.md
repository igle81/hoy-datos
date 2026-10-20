# hoy-datos

Datos públicos de **Hoy · AvilesIA** (https://hoy.avilesia.es). Los escribe un flujo de n8n en el VPS de AvilesIA; la web los lee a través de su función `api/datos.js`, que los valida (esquema y fecha, falla cerrado) antes de servirlos.

| Fichero | Qué es | Cuándo se actualiza | Fuente |
|---|---|---|---|
| `luz.json` | PVPC 2.0TD de hoy y, desde ~20:15, de mañana (€/kWh por hora) | 00:10 y 20:35 (hora de Madrid) | Red Eléctrica (REE), apidatos |
| `farmacias.json` | Guardias de hoy de los concejos de Asturias | cada hora | Colegio Oficial de Farmacéuticos de Asturias |
| `gasolina.json` | Media de gasolina 95 y gasóleo A a 10 km y las 5 más baratas, por municipio | a diario | Geoportal de carburantes (Ministerio para la Transición Ecológica) |

No edites a mano: lo sobrescribe el flujo. Un dato que no es de hoy no se sube (se queda el último bueno con su fecha y la web avisa).
