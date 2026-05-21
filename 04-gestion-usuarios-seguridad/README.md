
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

-- Privilegios globales (todo el servidor)
GRANT SUPER, PROCESS, SHOW DATABASES ON *.* TO 'dba'@'localhost';

-- Privilegios por base de datos
GRANT SELECT, INSERT, UPDATE, DELETE ON mi_bd.* TO 'app_user'@'localhost';

-- Privilegios por tabla
GRANT SELECT ON mi_bd.usuarios TO 'reportes'@'%';
GRANT UPDATE (email, telefono) ON mi_bd.usuarios TO 'soporte'@'%';

-- Privilegios por columna (MySQL 8.0+)
GRANT SELECT (id, nombre), UPDATE (estado) ON mi_bd.pedidos TO 'callcenter'@'%';

-- Rol (MySQL 8.0+)
CREATE ROLE 'lectura_solo';
GRANT SELECT ON mi_bd.* TO 'lectura_solo';
GRANT 'lectura_solo' TO 'analista1'@'%';
SET DEFAULT ROLE 'lectura_solo' TO 'analista1'@'%';

-- Ver privilegios
SHOW GRANTS FOR 'app_user'@'localhost';
SHOW GRANTS FOR CURRENT_USER();

-- Revocar privilegios
REVOKE INSERT, UPDATE ON mi_bd.* FROM 'app_user'@'localhost';
