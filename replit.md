# Overview

Lubricentro R/18 is a static HTML website for an automotive lubricant and oil change service center. The website serves as a digital catalog and information portal showcasing automotive products, services, and providing a purchase form for customers. It features a multi-page structure with product listings in different view formats (table and card layouts), detailed product pages, and a customer purchase form.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The application follows a traditional multi-page HTML structure with shared styling and navigation. Key architectural decisions include:

**Static HTML Structure**: Uses separate HTML files for each major page section, providing clear separation of concerns and simple navigation. This approach was chosen for simplicity and ease of maintenance without requiring a build process.

**Responsive CSS Design**: Implements a mobile-first responsive design using CSS Grid and Flexbox layouts. The styling uses a consistent design system with CSS custom properties for colors and spacing.

**Component-Based Styling**: CSS is organized with reusable component classes (`.btn`, `.product-box`, `.form-group`) that can be applied across different pages, promoting consistency and maintainability.

**Navigation System**: Consistent header navigation across all pages with active state indicators, providing clear user orientation and seamless page transitions.

## Page Structure
**Landing Page (index.html)**: Hero section with call-to-action buttons and service overview
**Product Catalog**: Dual-view system with table (`listado_tabla.html`) and card (`listado_box.html`) layouts for different user preferences
**Product Details (producto.html)**: Detailed product information with specifications and purchase options
**Purchase Form (comprar.html)**: Customer data collection with form validation

## Form Validation
Client-side validation using HTML5 attributes and custom JavaScript for enhanced user experience. Includes:
- **Nombre**: Solo letras y espacios permitidos
- **Teléfono**: Solo números permitidos (patrón: 3765100816)
- **Email**: Validación de formato estándar
- Validación en tiempo real con mensajes de error específicos
- Validación al envío del formulario para prevenir datos incorrectos

## Design System
**Racing / Automotriz Color Palette:**
- **Rojo intenso (#E60000)**: Botones, promociones, precios y elementos destacados
- **Negro carbón (#0F0F0F)**: Fondo principal, header, footer y contenedores
- **Gris metal (#B0B0B0)**: Bordes, secciones secundarias y elementos de apoyo
- **Blanco (#FFFFFF)**: Tipografía principal y elementos de contraste

Esta paleta proporciona una estética moderna de "taller/competición" con excelente legibilidad y contraste. La tipografía incluye efectos de sombra para mayor impacto visual.

# External Dependencies

## Styling Framework
**Custom CSS**: No external CSS frameworks used; all styling is custom-built for maximum control and minimal overhead.

## Assets and Resources
**No External CDNs**: All resources are self-contained within the project structure.
**No JavaScript Libraries**: Pure HTML5 and CSS3 implementation with minimal custom JavaScript for form validation.

## Third-Party Services
Currently, the application is fully self-contained with no external API integrations, payment processors, or analytics services. The purchase form appears to be designed for manual processing rather than automated order fulfillment.