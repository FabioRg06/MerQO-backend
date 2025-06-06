# MERCO

Proyecto backend profesional en Django, dockerizado y conectado a PostgreSQL.

## Requisitos
- Docker y Docker Compose
- Python 3.12 (solo para desarrollo local fuera de Docker)

## Configuración rápida

1. Copia el archivo `.env` si deseas personalizar las variables de entorno.
2. Construye y levanta los servicios:
   ```powershell
   docker-compose up --build
   ```
3. Accede a la app en http://localhost:8000

## Migraciones y superusuario
Para aplicar migraciones y crear un superusuario, ejecuta:
```powershell
docker-compose run web python manage.py migrate
docker-compose run web python manage.py createsuperuser
```

## Organización
- Código fuente Django: carpeta `MERCO/`
- Configuración Docker: `Dockerfile`, `docker-compose.yml`, `.env`
- Dependencias: `requirements.txt`

## Notas
- El entorno de base de datos está definido en variables de entorno y en `MERCO/settings.py`.
- Sigue las mejores prácticas de Django para mantener la organización y escalabilidad del proyecto.
