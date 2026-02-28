# BA Inmobiliaria Sur 🏙️
> **Directorio Inteligente de Inmobiliarias - Sur de CABA**

Repositorio oficial del sitio [bainmobiliaria.com.ar](https://www.bainmobiliaria.com.ar/). Una plataforma de nicho diseñada para conectar usuarios con inmobiliarias especializadas en el Distrito Tecnológico y los barrios de Barracas, Parque Patricios, San Telmo y Constitución.

## 🚀 Arquitectura Técnica (Serverless & Low-Cost)
Como solución de ingeniería, el proyecto aplica el concepto de **Jamstack**, eliminando la necesidad de servidores backend costosos y bases de datos tradicionales.

* **Frontend:** HTML5, CSS3 (vía Tailwind CSS) y Vanilla JavaScript (ES6+).
* **Data Source:** Google Sheets actuando como CMS Headless a través de una exportación dinámica en formato CSV.
* **Hosting:** GitHub Pages (Servicio de archivos estáticos de alta disponibilidad).
* **Performance:** Carga asincrónica de datos para un Time to First Byte (TTFB) optimizado.

## 🛠️ Cómo funciona
El sistema funciona bajo un flujo de sincronización en tiempo real:
1.  Los datos se administran desde una **Spreadsheet de Google Drive**.
2.  Al publicar la hoja como CSV, se genera un endpoint público.
3.  El cliente (navegador) realiza una petición `fetch()` al endpoint al cargar el sitio.
4.  Un script de parseo procesa el CSV y renderiza el directorio dinámicamente, permitiendo filtros de búsqueda sin recargar la página.

## 📂 Estructura del Proyecto
```text
/
├── index.html          # Aplicación Single Page (SPA) y lógica de negocio
├── CNAME               # Configuración del dominio personalizado (.com.ar)
└── README.md           # Documentación del sistema
