# 06 — Instalación de Odoo

1. Odoo S.A. cuenta con un repositorio que se puede usar para instalar la edición Community si ejecuta los siguientes comandos (sacados de la [documentación de Odoo](https://www.odoo.com/documentation/19.0/es/administration/on_premise/packages.html#repository)):

   ```bash
   wget -q -O - https://nightly.odoo.com/odoo.key | sudo gpg --dearmor -o /usr/share/keyrings/odoo-archive-keyring.gpg
   ```

   ```bash
   echo 'deb [signed-by=/usr/share/keyrings/odoo-archive-keyring.gpg] https://nightly.odoo.com/19.0/nightly/deb/ ./' | sudo tee /etc/apt/sources.list.d/odoo.list
   ```

   ```bash
   sudo apt-get update && sudo apt-get install odoo
   ```

2. Acto seguido ejecutamos ``apt-get upgrade`` para mantener la instalación actualizada.

   ```bash
   sudo apt-get upgrade
   ```
