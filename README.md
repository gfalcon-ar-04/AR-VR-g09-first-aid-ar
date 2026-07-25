# AR First Aid Assistant - RCP Guide

## Repositorio de Proyecto — PSISP08075 Realidad Virtual y Aumentada
### Universidad Autónoma del Perú | Ingeniería de Sistemas | 2026-1

---

## Descripción del Proyecto

**AR First Aid Assistant** es una aplicación móvil de Realidad Aumentada diseñada para guiar a personas sin formación médica en la ejecución correcta del protocolo de **Reanimación Cardiopulmonar (RCP)** en adultos. La app utiliza reconocimiento de imágenes (Vuforia Image Targets) para activar instrucciones visuales y auditivas paso a paso, superpuestas sobre el paciente en el entorno real.

El proyecto aborda el problema crítico del olvido o ejecución incorrecta de maniobras de RCP en situaciones de emergencia, proporcionando una herramienta accesible, interactiva y práctica para estudiantes, docentes y personal del campus universitario.

| Campo | Detalle |
|-------|---------|
| Tipo XR | Realidad Aumentada (RA) |
| Motor de desarrollo | Unity 2022.3.62f1 LTS |
| Tecnología AR | Vuforia Engine 10.21+ (Image Targets) |
| Lenguaje | C# |
| Plataforma | Android 8.0+ (API 26+) |
| Hardware mínimo | Cámara trasera, 3GB RAM |
| Curso | PSISP08075 — Realidad Virtual y Aumentada |
| Semestre | 2026-1 |

---

## Integrantes del Grupo

| Nombre | Código | Rol |
|--------|--------|-----|
| Retamozo Llamacponcca, Miguel Angel (100%) | 2221896924 | Líder del proyecto / Desarrollador Unity |
| Falcón Arones, Gabriel Adrián (100%) | 2221896310 | Documentación |
| Nuñez Cordova, Erick Ernesto (85%) | 2191891564 | Documentación |
| Estrada Gutierrez, Yohel Alexander (85%) | 2181894796 | Documentación |

---

## Funcionalidades Principales

- Reconocimiento de imágenes: Detecta tarjetas/pósters mediante Vuforia para activar el protocolo de RCP.
- Instrucciones paso a paso: Muestra secuencias textuales con los pasos correctos de RCP (verificar respuesta, pedir ayuda, inclinar cabeza, compresiones).
- Audio explicativo: Reproduce instrucciones de voz para cada paso, guiando al usuario sin necesidad de leer.
- Animación IK (Inverse Kinematics): El brazo del personaje se mueve automáticamente al pecho del paciente durante la RCP.

---

## Instalación y Uso

### Requisitos de Desarrollo

- Unity 2022.3.62f1 (LTS)
- Android SDK / NDK (instalado con Unity Hub)
- Licencia Vuforia (gratuita desde Vuforia Developer Portal)
- Android 8.0+ (API 26+) con cámara trasera

### Clonar el repositorio

bash
git clone https://github.com/RubenCarty/rva-g09-first-aid-ar.git
cd rva-g09-first-aid-ar
Abrir en Unity
Abrir Unity Hub.

Click en "Add" y seleccionar la carpeta del proyecto.
Abrir el proyecto con Unity 2022.3.62f1.
Esperar a que Unity compile todos los assets y paquetes.

Configurar Vuforia

Obtener una License Key gratuita desde Vuforia Developer Portal -> License Manager.

En Unity, seleccionar la AR Camera en la jerarquía.

En el inspector, hacer clic en "Open Vuforia Configuration".

Pegar la License Key en el campo App License Key.

Asegurarse de que la base de datos FirstAidTargets esté importada (Assets/Vuforia/).

Ejecutar en Android

Conectar un dispositivo Android con depuración USB habilitada.

En Unity, ir a File > Build Settings.

Seleccionar Android y hacer clic en Switch Platform.

En Player Settings:

Package Name: com.tugrupo.firstaidar

Minimum API Level: Android 8.0 (API 26)

XR Settings: Habilitar Vuforia Augmented Reality.

Hacer clic en Build and Run.

Permitir los permisos de cámara en el dispositivo.

Enfocar el marcador impreso para activar el contenido AR.

Progreso del Proyecto

Semanas	Hito	Estado

S01-S02	Investigación y planteamiento del problema + idea inicial	Completado
S03-S04	Definición del MVP + arquitectura técnica	Completado
S05-S06	Prototipo básico funcional (Image Target + texto)	Completado
S07-S08	Implementación de RCPController, Audio, Temporizador	Completado
S09-S10	Animación IK para el brazo, Teletransporte	Completado
S11-S12	Pruebas de usabilidad, corrección de errores	Completado
S13-S14	Exportación a Android, pruebas en dispositivo	Completado
S15-S16	Proyecto final + presentación	Completado

Estructura del Repositorio

rva-g09-first-aid-ar/
├── Assets/
│   ├── _Project/
│   │   ├── Scenes/          <- Escenas (MenuScene, GameScene)
│   │   ├── Scripts/         <- Scripts C# (FPSController, RCPController, etc.)
│   │   ├── Prefabs/         <- Prefabs (Player, ImageTarget, etc.)
│   │   ├── Materials/       <- Materiales y shaders
│   │   ├── Audio/           <- Clips de audio para instrucciones
│   │   ├── UI/              <- Assets de interfaz (fuentes, iconos)
│   │   └── Vuforia/         <- Bases de datos de Image Targets
│   └── ...
├── docs/
│   ├── informe_final.pdf    <- Documentación completa del proyecto
│   ├── arquitectura.md      <- Diagramas y descripción técnica
│   ├── usabilidad.md        <- Resultados de pruebas con usuarios
│   └── capturas/            <- Screenshots del proyecto
├── Packages/                <- Manifest de paquetes Unity
├── ProjectSettings/         <- Configuración del proyecto
├── .gitignore               <- Excluye archivos temporales de Unity
└── README.md                <- Este archivo

Tecnologías Utilizadas
Tecnologia	Version	Uso
Unity	2022.3.62f1 LTS	Motor de juego y desarrollo
Vuforia Engine	10.21+	Reconocimiento de imagenes y tracking AR
Animation Rigging	1.3.0+	Control de IK para animacion del brazo
TextMeshPro	3.0+	Texto en 3D y UI de alta calidad
Android SDK	API 26+	Exportacion a dispositivo movil

Referencias

Vuforia Developer Portal. (2024). Vuforia Engine Documentation.

Unity Technologies. (2023). Unity 2022.3 LTS Documentation.

Unity Technologies. (2023). Animation Rigging Package Documentation.

Sociedad Americana del Corazon. (2020). Guia de RCP y atencion cardiovascular de emergencia.

Licencia

Proyecto academico desarrollado para el curso PSISP08075 - Realidad Virtual y Aumentada de la Universidad Autonoma del Peru. Uso exclusivamente educativo.
