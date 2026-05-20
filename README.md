# 🗄️ Curso Completo de Administración de Bases de Datos (DBA)

[![Licencia](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)
[![Estado](https://img.shields.io/badge/Estado-En%20Desarrollo-green.svg)]()
[![Contribuciones](https://img.shields.io/badge/Contribuciones-Bienvenidas-brightgreen.svg)](CONTRIBUTING.md)

> **De principiante a DBA profesional**: Aprende a administrar, optimizar y asegurar bases de datos empresariales

## 📋 Tabla de Contenidos
- [🎯 ¿Para quién es este curso?](#-para-quién-es-este-curso)
- [📚 Temario Completo](#-temario-completo)
- [🚀 Inicio Rápido](#-inicio-rápido)
- [🛠️ Tecnologías Cubiertas](#️-tecnologías-cubiertas)
- [📖 Cómo usar este repositorio](#-cómo-usar-este-repositorio)
- [🤝 Contribuir](#-contribuir)
- [📜 Licencia](#-licencia)

## 🎯 ¿Para quién es este curso?
- **Administradores de sistemas** que quieren especializarse en BD
- **Desarrolladores** que desean entender el rendimiento de sus queries
- **Estudiantes de informática** que buscan preparación práctica
- **Junior DBAs** que necesitan una guía estructurada

**Requisitos previos:**
- Conocimientos básicos de SQL
- Familiaridad con línea de comandos
- Conceptos básicos de redes

## 📚 Temario Completo

### Módulo 1: Introducción a la Administración de BD
- Rol y responsabilidades del DBA
- Tipos de bases de datos (Relacionales vs NoSQL)
- Ciclo de vida de una BD empresarial

### Módulo 2: Instalación y Configuración
- [MySQL/PostgreSQL](./02-instalacion-configuracion/mysql-postgres.md)
- [SQL Server/Oracle](./02-instalacion-configuracion/sqlserver-oracle.md)
- Configuración de parámetros críticos
- Variables de entorno y paths

### Módulo 3: Arquitectura Interna
- Motor de almacenamiento (InnoDB, MyISAM)
- Procesos y memoria en PostgreSQL
- Archivos de datos, logs y control files
- Estructura de páginas y bloques

### Módulo 4: Gestión de Usuarios y Seguridad
- Creación y gestión de roles/perfiles
- Políticas de contraseñas
- Autenticación y autorización
- Auditoría básica
- Encriptación en reposo y tránsito

### Módulo 5: Backup y Recovery ⭐
- [Scripts de backup automáticos](./05-backup-recovery/)
- Tipos de backup: FULL, INCREMENTAL, DIFFERENTIAL
- PITR (Point In Time Recovery)
- Verificación de integridad
- **Ejercicio práctico:** Simula una pérdida de datos y recupera

### Módulo 6: Monitoreo y Tuning de Rendimiento
- Identificar queries lentos (slow query log)
- Índices: cuándo y cómo crearlos
- Análisis de planes de ejecución
- Métricas clave (QPS, hit ratio, lock waits)

### Módulo 7: Alta Disponibilidad y Escalabilidad
- Replicación Master-Slave
- Clustering (Galera, Patroni)
- Load balancing
- Sharding vs Particionamiento

### Módulo 8: Automatización para DBAs
- Scripts con Bash/Python
- Tareas programadas (cron jobs)
- Alertas por correo/Slack
- Health checks automáticos

## 🚀 Inicio Rápido

### Clona el repositorio
```bash
git clone https://github.com/Hugo214/administracion_de_base_de_datos.git
cd administracion_de_base_de_datos
