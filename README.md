

Claro, aquí tienes una propuesta de `README.md` para el proyecto **Nomowi Calendar**, manteniendo el estilo profesional y detallado de los ejemplos anteriores, pero adaptado a la naturaleza específica de este proyecto como un módulo.

---

# 📅 Nomowi Calendar - Calendario modular para el ecosistema Mizu OS

> "El calendario del proyecto NOMOWI, reimaginado como un módulo independiente para Mizu OS. Simple, ligero y listo para integrar."

![Versión](https://img.shields.io/badge/versión-1.2.0--mizu-green)
![Licencia](https://img.shields.io/badge/licencia-MIT-blue)
![Tecnología](https://img.shields.io/badge/tecnología-Mizu_Frameworks-purple)
![Estado](https://img.shields.io/badge/status/estable-brightgreen)
![Arquitectura](https://img.shields.io/badge/arquitectura-modular-orange)

---

## 🌐 Demo en vivo

👉 [Disponible como módulo dentro de Mizu OS](https://mizulegendsstudios.github.io/mizu-os/)

---

## 🌟 Visión del Proyecto

Nomowi Calendar nació como una pieza fundamental del proyecto NOMOWI, enfocándose en la simplicidad y la funcionalidad esencial de un calendario. Hoy, evoluciona hacia una nueva rama: un módulo completamente compatible y optimizado para el ecosistema de **Mizu OS**.

La versión `1.2.0-mizu` prioriza la **integración**, la **ligereza** y la **autonomía**, permitiendo a los usuarios de Mizu OS añadir una funcionalidad de calendario robusta sin la complejidad de una aplicación monolítica.

---

### 📅 Características / Roadmap

| Característica      | Estado   | Notas clave                                                     |
| ------------------- | -------- | --------------------------------------------------------------- |
| 🗓️ Vista Mensual    | ✅ Estable | Navegación intuitiva entre meses.                               |
| ➕ Gestión de Eventos | ✅ Estable | Crear, editar y eliminar eventos básicos.                        |
| 🔌 Integración Mizu OS | ✅ Estable | Se registra y funciona como una app nativa de Mizu OS.         |
| 🔄 Sincronización    | 🚧 Plan   | Sincronización con calendarios externos (via API/ICS).          |
| 📆 Vista Semanal/Agenda | 🚧 Plan   | Vista detallada por días y semanas.                             |
| 🔔 Recordatorios     | 🚧 Plan   | Notificaciones para eventos próximos.                            |
| 🎨 Temas Personalizables | 🚧 Plan   | Adaptación a la apariencia de Mizu OS.                          |

---

## 🏗️ Arquitectura Técnica (v1.2.0-mizu)
### Principios Fundamentales

    ✅ Integración First: Diseñado para funcionar sin problemas dentro de Mizu OS.
    ✅ Ligero y Autónomo: Mínimo impacto en el rendimiento del sistema principal.
    ✅ Compatible con Mizu Frameworks: Aprovecha el EventBus, el AppRegistry y el sistema de contenedores de Mizu OS.
    ✅ Sin Dependencias Externas: Construido con Vanilla JS, CSS y HTML, alineado con la filosofía de Mizu.
    ✅ Licencia permisiva: MIT — Fomenta la reutilización y la integración en otros proyectos.

### 🔄 Evolución Arquitectónica

La transición de Nomowi Calendar ha sido de un componente acoplado a un módulo descentralizado y reutilizable.
```text
Antigua (Componente NOMOWI):
NOMOWI App Suite → Nomowi Calendar (acoplado al sistema principal)

Nueva (Módulo Mizu OS):
Mizu OS → AppRegistry → Nomowi Calendar (módulo independiente)
                       │
                       ├── bootstrap.js (auto-registro)
                       ├── appcore.js (lógica del calendario)
                       └── manifest.json (metadatos para Mizu)
```
 
**Ventajas de la nueva arquitectura:**
- ✅ **Desacoplamiento Total**: Puede ser actualizado o reemplazado sin afectar a Mizu OS.
- ✅ **Portabilidad**: Fácil de integrar en otros proyectos (incluso via iFrame).
- ✅ **Mantenimiento Simplificado**: El código es más pequeño y enfocado.
- ✅ **Carga Bajo Demanda**: Solo se carga cuando el usuario lo solicita.
- ✅ **Ecosistema Compatible**: Habla el mismo "lenguaje" que otras apps de Mizu OS.

### 📦 Stack Tecnológico
```text
// Tecnologías principales
- ES6+ JavaScript (módulos nativos)
- CSS3 con Custom Properties (hereda de Mizu OS)
- HTML5 APIs (Date, LocalStorage)

// Estructura de módulos
Nomowi Calendar → Core Logic → [Event Manager, Date Renderer, UI Controller] → Mizu OS AppRegistry
```

---

## 🗂️ Estructura del Proyecto
```text
nomowi-calendar/
├─ LICENSE                                     # MIT
├─ README.md                                   # Este archivo
├─ manifest.json                               # Manifiesto para Mizu OS
├─ index.html                                  # Entry-point para uso standalone/iFrame
├─ src/
│  ├─ core.js                                  # Lógica principal del calendario
│  ├─ styles.css                               # Estilos del componente
│  ├─ bootstrap.js                             # Auto-registro en Mizu OS
│  └─ assets/
│     └─ icons/                                # Iconos de la aplicación
└─ dist/                                       # Versión compilada/lista para producción
   └─ nomowi-calendar.bundle.js                # (Opcional, si se decide minificar)
```

---

## 🎯 Características técnicas actuales (v1.2.0-mizu)
### ✅ Implementado

**NÚCLEO DEL CALENDARIO**
       
    - 🗓️ Renderizado eficiente del calendario mensual.
    - 🖱️ Navegación intuitiva entre meses y años.
    - 📅 Resaltado del día actual.
    - ➕ Interfaz modal para la creación y edición de eventos.
    - 💾 Almacenamiento local de eventos usando `localStorage`.
    - 🎨 Estilos que se adaptan al tema de Mizu OS usando CSS Custom Properties.

**INTEGRACIÓN CON MIZU OS**
    
    - 📦 `bootstrap.js`: Se registra automáticamente en el `AppRegistry` de Mizu OS.
    - 📡 `EventBus`: Escucha eventos del sistema (ej. `theme-changed`) para adaptarse.
    - 🗂️ `AppContainerManager`: Se renderiza dentro de un contenedor de aplicación estándar de Mizu.
    - 📱 Totalmente responsivo dentro del ecosistema de Mizu OS.

### 🔄 En Desarrollo 

**FUNCIONALIDADES**

    - [ ] Vista de semana y día.
    - [ ] Sistema de recordatorios con notificaciones del navegador.
    - [ ] Importación/Exportación de calendarios en formato `.ics`.
    - [ ] Soporte para eventos recurrentes (diarios, semanales, mensuales).
    - [ ] Categorías y colores para eventos.

---

## 🚀 Instalación y Uso

Nomowi Calendar es flexible y puede usarse de dos maneras principales.

### Opción 1: Como Módulo de Mizu OS (Recomendado)

Integra el calendario directamente en tu instalación local de Mizu OS para una experiencia nativa.

1.  **Clonar el repositorio del calendario:**
    ```bash
    git clone https://github.com/nomowi-project/nomowi-calendar.git
    ```
2.  **Mover al directorio de apps de Mizu OS:**
    Copia la carpeta `nomowi-calendar` (resultante del clonado) dentro del directorio `docs/apps/` de tu instalación de Mizu OS.
    ```text
    mizu-os/docs/apps/nomowi-calendar/
    ```

3.  **Iniciar Mizu OS:**
    Al iniciar Mizu OS, el `bootstrap.js` de Nomowi Calendar se registrará automáticamente y aparecerá en el lanzador de aplicaciones.

### Opción 2: Integración Manual via iFrame

Incrusta el calendario en cualquier sitio web, de forma independiente a Mizu OS.

1.  **Descarga y descomprime:**
    Descarga la última versión desde [Releases](https://github.com/nomowi-project/nomowi-calendar/releases) y descomprimela en un directorio accesible por tu servidor web.

2.  **Insertar con un iframe:**
    Copia y pega el siguiente código HTML en la página donde quieras mostrar el calendario. Asegúrate de que la ruta `src` apunte a la ubicación correcta del archivo `index.html`.

    ```html
    <iframe 
      src="ruta/a/tu/nomowi-calendar/index.html" 
      style="width: 100%; height: 600px; border: 1px solid #ccc; border-radius: 8px;"
      title="Nomowi Calendar">
    </iframe>
    ```

---

## 📜 Licencia 

Este proyecto está bajo MIT License — Usa, modifica y redistribuye libremente. Ver [LICENSE](./LICENSE) para detalles completos.

Copyright (c) 2025 Proyecto NOMOWI

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

### 🧭 Filosofía del Proyecto 

    Prioridad #1: Simplicidad y facilidad de uso.
    Regla #1: Una cosa, y hacerla bien (ser un gran calendario).
    Stack: Alineado con Mizu OS (HTML, CSS, JS plano).
    Entorno: Modular, tanto en la nube como localmente.

---

## 👥 Contribución

¡Las contribuciones son bienvenidas! Si quieres mejorar Nomowi Calendar, por favor, abre un *issue* para discutir los cambios o envía un *pull request*.

1.  Fork el proyecto.
2.  Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`).
3.  Commit tus cambios (`git commit -m 'feat: añadir nueva funcionalidad'`).
4.  Push a la rama (`git push origin feature/nueva-funcionalidad`).
5.  Abre un Pull Request.

---

## 🌐 Soporte y Comunidad

📋 Reportar Issues: [Github Issues](https://github.com/nomowi-project/nomowi-calendar/issues)

📘 Documentación: [Wiki del Proyecto](https://github.com/nomowi-project/nomowi-calendar/wiki)

💬 Únete a la comunidad original de NOMOWI en Facebook para discutir ideas y obtener ayuda:

[Comunidad de Nomowi en fb](https://www.facebook.com/groups/nomowi/ "Nomowi")

---

Nomowi Calendar - Organiza tu tiempo, en el ecosistema que elijas. 🚀

    © 2025 Proyecto NOMOWI & Comunidad Mizu OS — Construido con simplicidad y para la comunidad.
