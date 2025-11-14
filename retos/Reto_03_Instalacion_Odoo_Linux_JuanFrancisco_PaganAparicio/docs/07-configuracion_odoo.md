# 07 — Configuración de Odoo (`/etc/odoo/odoo.conf`)

1. Abrimos el siguiente **archivo**:

   ```bash
   sudo nano /etc/odoo/odoo.conf
   ```

2. Edita el archivo de **configuración** con:

   ```ini
   [options]
   db_host = 127.0.0.1 ; localhost
   db_port = 5432 ; puerto de postgres
   db_user = odoo ; usuario que hayamos creado para odoo
   db_password = odoo ; contraseña que le hayamos dado al usuario odoo
   addons_path = /opt/odoo/odoo-src/addons
   logfile = /var/log/odoo/odoo.log
   xmlrpc_port = 8069 ; puerto por defecto de Odoo
   ```

3. Crea **carpetas** y **permisos** si procede:

   ```bash
   sudo mkdir -p /var/log/odoo && sudo chown odoo:odoo /var/log/odoo
   ```

4. **Reiniciamos** el servicio de **Odoo**:

   ```bash
   service odoo restart && service odoo status
   ```
