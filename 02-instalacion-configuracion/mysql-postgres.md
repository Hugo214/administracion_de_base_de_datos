# Módulo 2: Instalación y Configuración - MySQL & PostgreSQL

## Instalación de MySQL 8.0

### En Ubuntu/Debian
```bash
# Actualizar repositorios
sudo apt update

# Instalar MySQL Server
sudo apt install mysql-server -y

# Verificar estado
sudo systemctl status mysql

# Configuración inicial de seguridad
sudo mysql_secure_installation
