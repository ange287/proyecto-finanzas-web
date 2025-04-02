# Documentación de la Aplicación "Finanzas Personales"

## Descripción General
La aplicación "Finanzas Personales" es una herramienta web diseñada para gestionar transacciones financieras, estimaciones de gastos, categorías y gráficos interactivos. La aplicación utiliza IndexedDB para el almacenamiento local y Chart.js para las visualizaciones.

## Estructura del Proyecto

### Archivos Principales

#### 1. index.html
- Punto de entrada de la aplicación
- Define la estructura básica del HTML
- Incluye las dependencias externas (Chart.js, Font Awesome)
- Contiene el contenedor principal `<div id="app">`
- Carga los estilos y scripts necesarios

### Estilos (CSS)

#### 2. css/styles.css
- Estilos generales de la aplicación
- Define la paleta de colores y tipografía
- Implementa diseño responsivo
- Estilos para formularios y componentes UI
- Animaciones y transiciones

#### 3. css/charts.css
- Estilos específicos para gráficos
- Personalización de Chart.js
- Diseño de contenedores de gráficos
- Estilos para leyendas y tooltips

### JavaScript - Core

#### 4. js/app.js
Archivo principal que inicializa y coordina toda la aplicación:
- **Clase App**:
  - Constructor: Inicializa componentes y estado inicial
  - init(): Configura la base de datos y carga datos iniciales
  - render(): Estructura principal de la UI
  - handleTabChange(): Gestión de pestañas
  - Métodos para manejar transacciones y estimaciones
  - Actualización de gráficos y sidebar
  - Gestión de errores y estado global

#### 5. js/db.js
Gestión de la base de datos IndexedDB:
- Inicialización de la base de datos
- Definición de object stores
- Operaciones CRUD para cada entidad
- Manejo de versiones y migraciones
- Funciones de utilidad para consultas

### JavaScript - Servicios

#### 6. js/services/UIService.js
Servicios de interfaz de usuario:
- Formateo de fechas y moneda
- Mensajes de éxito/error
- Utilidades de renderizado
- Gestión de elementos DOM
- Formateo de nombres y valores

#### 7. js/services/TransactionService.js
Gestión de transacciones:
- CRUD de transacciones
- Cálculo de balances
- Procesamiento de datos para gráficos
- Filtrado y ordenamiento
- Validación de datos

#### 8. js/services/EstimateService.js
Gestión de estimaciones:
- CRUD de estimaciones
- Comparación con gastos reales
- Cálculos de proyecciones
- Validación de estimaciones
- Procesamiento para reportes

#### 9. js/services/ChartService.js
Servicios de visualización:
- Configuración de Chart.js
- Generación de gráficos
- Actualización en tiempo real
- Personalización de visualizaciones
- Procesamiento de datos para gráficos

#### 10. js/services/CategoryService.js
Gestión de categorías:
- CRUD de categorías
- Categorías predefinidas
- Validación y normalización
- Relaciones con transacciones
- Gestión de jerarquías

### JavaScript - Componentes

#### 11. js/components/TransactionForm.js
Formulario de transacciones:
- Renderizado del formulario
- Validación de entrada
- Gestión de eventos
- Filtros de transacciones
- Lista de transacciones
- Eliminación de transacciones

#### 12. js/components/EstimateForm.js
Formulario de estimaciones:
- Renderizado del formulario
- Validación de estimaciones
- Gestión de períodos
- Lista de estimaciones
- Comparación con gastos reales

#### 13. js/components/Sidebar.js
Barra lateral de navegación:
- Mostrar balance actual
- Navegación entre pestañas
- Resumen de ingresos/gastos
- Estado activo/inactivo
- Actualización en tiempo real

#### 14. js/components/ChartPanel.js
Panel de gráficos:
- Múltiples tipos de gráficos
- Interactividad
- Actualización dinámica
- Opciones de visualización
- Exportación de datos

#### 15. js/components/CategoryManager.js
Gestor de categorías:
- CRUD de categorías
- Restauración de predefinidas
- Validación de nombres
- Actualización de selectores
- Gestión de relaciones

## Flujo de Datos
1. La aplicación se inicializa en app.js
2. Se configura la base de datos en db.js
3. Los servicios manejan la lógica de negocio
4. Los componentes renderizan la UI y manejan interacciones
5. Los cambios se persisten en IndexedDB
6. La UI se actualiza en tiempo real

## Características Principales
- Gestión de transacciones y estimaciones
- Categorización de gastos
- Visualizaciones interactivas
- Almacenamiento local
- Interfaz responsiva
- Validación de datos
- Manejo de errores
- Actualizaciones en tiempo real

## Tecnologías Utilizadas
- HTML5
- CSS3
- JavaScript (ES6+)
- IndexedDB
- Chart.js
- Font Awesome

## Mejores Prácticas Implementadas
- Arquitectura modular
- Separación de responsabilidades
- Manejo asíncrono con async/await
- Validación de datos
- Manejo de errores
- Comentarios descriptivos
- Código mantenible y escalable
