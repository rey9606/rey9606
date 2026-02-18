# Portfolio Data

Este archivo contiene todos los datos de tu portafolio en un único JSON.

## Estructura del Archivo

### profile
Datos personales y profesionales:
- `name`: Tu nombre completo
- `title`: Tu título profesional
- `description`: Descripción breve
- `image`: Ruta a tu foto de perfil (ej: `profile/perfil.webp`)
- `heroImage`: Ruta a imagen hero
- `socialLinks`: Array de enlaces a redes sociales
- `status`: Estado de disponibilidad ('available', 'busy', 'unavailable')
- `whatsappNumber`: Número de WhatsApp (sin +)
- `email`: Email de contacto

### experience
Array de experiencias laborales. Cada objeto contiene:
- `id`: Identificador único
- `company`: Nombre de la empresa
- `location`: Ubicación/remoto
- `type`: Tipo ('full-time', 'freelance', 'project')
- `color`: Color de acento ('blue', 'purple', 'green', 'orange', 'red', 'cyan')
- `icon`: Icono representativo
- `technologies`: Array de tecnologías
- `roles`: (opcional) Array de roles si es una empresa con múltiples posiciones

### projects
Array de proyectos. Cada proyecto contiene:
- `nombre`: Nombre del proyecto
- `cliente`: Cliente o contexto
- `periodo`: Período de desarrollo
- `descripcion`: Descripción completa
- `rol`: Tu rol en el proyecto
- `tecnologias`: Array de tecnologías usadas
- `logros`: Array de logros con titulo, descripcion, metrica
- `assets`: Nombre de carpeta para imágenes (opcional)
- `link_demo`: URL demo (opcional)
- `repositorio`: URL repositorio (opcional)

### skills
Ábol de habilidades técnicas:
- `nodes`: Nodos de habilidades
- `edges`: Conexiones entre habilidades

### config
Configuración del portafolio:
- `github.dataRepo`: Repo de datos (formato: `usuario/repo`)
- `github.branch`: Rama del repo
- `github.assetsPath`: Ruta a los assets
- `features`: Features habilitadas

## Imágenes

Las imágenes deben estar en la carpeta `assets` de tu repositorio de datos:
```
assets/
  profile/
    perfil.webp
    img1.webp
  projects/
    linki/
      img0.webp
      icon.png
    pos/
      img0.webp
```

## Cómo Usar

1. Crea un repositorio nuevo en GitHub (ej: `tu-usuario/portfolio-data`)
2. Copia este archivo como `portfolio.json`
3. Agrega tus imágenes en la carpeta `assets`
4. En este proyecto, configura el repo en `src/environments/environment.ts`
5. Despliega y los datos se cargarán automáticamente desde tu repositorio

## Notas

- Los datos locales en `data-source/` se usan como fallback si no se puede cargar desde GitHub
- El portafolio funciona sin configuración externa usando los datos locales por defecto
