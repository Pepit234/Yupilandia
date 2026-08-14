# Survival Client — Minecraft Java 1.21.8

**Cliente/mod de supervivencia legítima** para Minecraft Java Edition **1.21.8** (exacto).

Desarrollado con **Fabric + Fabric API**, Java 21, Yarn mappings.

## Características implementadas (legítimas)

### HUD
- Coordenadas X/Y/Z
- Dirección (N/S/E/O)
- FPS
- Ping (multiplayer)
- Vida y hambre
- Armadura
- Durabilidad del objeto en mano
- Efectos activos + tiempo restante
- Hora del mundo
- Dimensión
- Bioma (cuando la API lo permite)

Todo configurable (activar/desactivar, posición, escala, color) vía `config/survivalclient.json`.

### Waypoints
- Crear waypoint en la posición actual (tecla **B**)
- Nombre, coordenadas, color, dimensión
- Guardado local
- Distancia calculable

### Supervivencia
- Avisos de durabilidad baja (configurable, umbral %)
- Información de estado del jugador

### Arquitectura modular
- `core` — inicialización y ModuleManager
- `hud` — interfaz
- `survival` — avisos y estado
- `exploration` — waypoints
- `inventory` — información de inventario (solo lectura)
- `building` — calculadora de materiales (esqueleto)
- `performance` — optimizaciones seguras
- `config` — JSON local
- `ui` — keybindings y menús
- `util` — constantes

## Controles por defecto
| Tecla          | Acción                          |
|----------------|---------------------------------|
| Right Shift    | Abrir menú (esqueleto)          |
| B              | Añadir waypoint en tu posición  |
| H              | Activar / desactivar HUD        |

## Requisitos
- Minecraft Java **1.21.8**
- Fabric Loader ≥ 0.16.14
- Fabric API (compatible 1.21.8)
- Java 21

## Cómo compilar

```bash
# Clonar o copiar el proyecto
cd SurvivalClient

# Generar el jar
./gradlew build
```

El archivo resultante estará en:
`build/libs/survivalclient-1.0.0.jar`

Colócalo en la carpeta `mods` junto con Fabric API.

## Configuración
Archivo: `.minecraft/config/survivalclient.json`

Se crea automáticamente con valores por defecto. Si está corrupto, se regenera.

## Seguridad y reglas
- **Cero cheats**: No hay Aimbot, KillAura, Fly, X-Ray, ESP, Reach, Speed, NoClip, AutoClicker, packet manipulation, duplicación de items ni nada ilegal.
- Todo funciona solo con APIs públicas del cliente.
- No se leen tokens, sesiones, cookies ni datos personales.
- No se modifican cuentas ni se envía información externa.

## Limitaciones legítimas
Algunas funciones solicitadas (brújula visual avanzada, calculadora de materiales completa, menú GUI profesional con drag & drop, import/export de waypoints, perfiles de configuración avanzados, etc.) requieren más desarrollo de UI.

Este proyecto entrega:
1. Estructura completa y correcta para 1.21.8
2. Sistema modular profesional
3. HUD funcional y configurable
4. Waypoints básicos funcionales
5. Avisos de durabilidad
6. Configuración local robusta
7. Keybindings
8. Código limpio y documentado

Puedes expandir fácilmente cualquier módulo siguiendo el mismo patrón `Module`.

## Licencia
MIT
