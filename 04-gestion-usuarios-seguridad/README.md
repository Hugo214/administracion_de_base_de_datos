
---

## `04-gestion-usuarios-seguridad/README.md`

```markdown
# Módulo 4: Gestión de Usuarios y Seguridad

## Objetivos
- Implementar control de acceso granular
- Aplicar principio de mínimo privilegio
- Configurar auditoría básica

## Gestión de Usuarios en MySQL

### Creación y gestión
```sql
-- Crear usuario básico
CREATE USER 'app_user'@'localhost' IDENTIFIED BY 'SecurePass123!';
CREATE USER 'app_web'@'192.168.1.%' IDENTIFIED BY 'WebPass456!';

-- Crear con expiración de password
CREATE USER 'temp_user'@'%' IDENTIFIED BY 'TempPass789!' PASSWORD EXPIRE INTERVAL 90 DAY;

-- Modificar usuario
ALTER USER 'app_user'@'localhost' IDENTIFIED BY 'NewPass123!';
ALTER USER 'app_user'@'localhost' PASSWORD EXPIRE;

-- Eliminar usuario
DROP USER 'app_user'@'localhost';
