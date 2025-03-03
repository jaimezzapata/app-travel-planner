# 🗺️ Travel Planner

## 📌 Descripción del Proyecto
Travel Planner es una aplicación web desarrollada en **React + Vite** que permite a los usuarios planificar viajes internacionales de manera organizada. La app ayuda a registrar información clave como país de origen y destino, presupuesto, gastos detallados (alojamiento, transporte, comida, actividades) y requisitos de entrada como visa y vacunas. Además, la aplicación realiza conversiones de moneda automáticamente basándose en la tasa de cambio definida.

## 🚀 Tecnologías Utilizadas
- **React** (Vite) - Desarrollo del frontend
- **React Router** - Manejo de rutas
- **JSON-Server** - Backend simulado para almacenar datos
- **Fetch API / Axios** - Consumo de datos desde JSON-Server
- **Tailwind CSS o CSS personalizado** - Estilización de la interfaz

## 📌 Planteamiento del Problema
Planificar un viaje internacional puede ser complejo, ya que involucra múltiples factores como:
✔️ Presupuesto y gastos detallados en distintas monedas.  
✔️ Fechas de entrada y salida de alojamientos.  
✔️ Documentos y requisitos de entrada según el país destino.  
✔️ Historial de viajes pasados.  

Con esta aplicación, los usuarios pueden organizar toda esta información en un solo lugar y visualizar los detalles de su viaje fácilmente.

## 📂 Modelo de Datos (`db.json`)
La base de datos simulada en **JSON-Server** tiene la siguiente estructura:

```json
{
  "viajes": [
    {
      "id": 1,
      "pais_origen": "Colombia",
      "moneda_origen": "COP",
      "pais_destino": "Japón",
      "ciudad_destino": "Tokio",
      "fecha_salida": "2025-07-10",
      "fecha_regreso": "2025-07-25",
      "presupuesto": 8000000,
      "moneda_destino": "JPY",
      "tasa_conversion": 0.024,
      "requisitos": [
        { "nombre": "Visa de turista", "obligatorio": true },
        { "nombre": "Vacuna contra fiebre amarilla", "obligatorio": false }
      ],
      "gastos": [
        {
          "id": 1,
          "categoria": "Alojamiento",
          "nombre_lugar": "Hotel Sakura",
          "ciudad": "Tokio",
          "fecha_ingreso": "2025-07-11",
          "fecha_salida": "2025-07-18",
          "dias": 7,
          "descripcion": "Habitación doble con desayuno incluido",
          "monto": 70000,
          "moneda": "JPY",
          "monto_convertido": 1680
        }
      ]
    }
  ]
}
```

## 📂 Estructura del Proyecto
```
📂 travel-planner  (Nombre del proyecto)
 ┣ 📂 public       # Archivos estáticos (favicon, imágenes, etc.)
 ┣ 📂 src          # Código fuente del proyecto
 ┃ ┣ 📂 assets     # Recursos como imágenes, estilos, fuentes
 ┃ ┣ 📂 components # Componentes reutilizables
 ┃ ┃ ┣ 📜 Navbar.jsx
 ┃ ┃ ┣ 📜 Footer.jsx
 ┃ ┃ ┣ 📜 TravelCard.jsx         # Tarjeta con resumen de un viaje
 ┃ ┃ ┣ 📜 TravelForm.jsx         # Formulario para agregar un nuevo viaje
 ┃ ┃ ┣ 📜 TravelList.jsx         # Lista de viajes creados
 ┃ ┃ ┣ 📜 TravelDetail.jsx       # Detalles de un viaje con gastos y requisitos
 ┃ ┃ ┣ 📜 ExpenseForm.jsx        # Formulario para agregar gastos
 ┃ ┃ ┣ 📜 ExpenseList.jsx        # Lista de gastos con detalles
 ┃ ┃ ┣ 📜 Requirements.jsx       # Muestra requisitos de entrada (visa, vacunas)
 ┃ ┃ ┣ 📜 CurrencyConverter.jsx  # Conversión de moneda entre origen y destino
 ┃ ┣ 📂 pages      # Vistas principales
 ┃ ┃ ┣ 📜 Home.jsx             # Página principal con lista de viajes
 ┃ ┃ ┣ 📜 TravelPage.jsx       # Página de detalles de un viaje
 ┃ ┃ ┗ 📜 NotFound.jsx         # Página 404 si no encuentra la ruta
 ┃ ┣ 📂 services   # Conexión con la API (JSON-Server)
 ┃ ┃ ┗ 📜 api.js               # Archivo para manejar peticiones a JSON-Server
 ┃ ┣ 📂 router     # Configuración de rutas
 ┃ ┃ ┗ 📜 index.jsx           # Definición de rutas con React Router
 ┃ ┣ 📂 styles     # Archivos de estilos
 ┃ ┃ ┗ 📜 global.css          # Estilos globales
 ┃ ┣ 📜 App.jsx               # Componente principal
 ┃ ┣ 📜 main.jsx              # Punto de entrada de React
 ┣ 📜 .gitignore              # Archivos a ignorar en Git
 ┣ 📜 package.json            # Dependencias y scripts del proyecto
 ┣ 📜 vite.config.js          # Configuración de Vite
 ┗ 📜 README.md               # Documentación del proyecto
```

## 🔧 Instalación y Ejecución del Proyecto
### 1️⃣ Clonar el repositorio
```sh
git clone https://github.com/tuusuario/travel-planner.git
cd travel-planner
```

### 2️⃣ Instalar dependencias
```sh
npm install
```

### 3️⃣ Configurar y ejecutar JSON-Server
```sh
npm install -g json-server
json-server --watch db.json --port 5000
```
Esto iniciará un servidor en `http://localhost:5000/` para simular una API.

### 4️⃣ Iniciar el proyecto con Vite
```sh
npm run dev
```
Esto ejecutará la aplicación en `http://localhost:5173/` o en el puerto que asigne Vite.

## 🎯 Contribuciones
Si deseas contribuir, puedes enviar un pull request o abrir un issue con sugerencias y mejoras.

## 📝 Licencia
Este proyecto es de código abierto y está bajo la licencia MIT.

---

🔥 **Listo para usar!** 🚀 Si necesitas más detalles, dime qué agregar. 😃

