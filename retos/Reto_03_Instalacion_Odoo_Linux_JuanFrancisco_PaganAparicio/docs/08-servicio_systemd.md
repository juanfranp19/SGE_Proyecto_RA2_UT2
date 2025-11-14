# 08 — Servicio systemd (`odoo.service`)

1. Crea el servicio en `/etc/systemd/system/odoo.service`:

   ```bash
   sudo nano /etc/systemd/system/odoo.service
   ```

   ```ini
   [Unit]
   Description=Odoo Service
   After=network.target postgresql.service

   [Service]
   Type=simple
   User=odoo
   Group=odoo
   ExecStart=/opt/odoo/venv/bin/python /opt/odoo/odoo-src/odoo-bin -c /etc/odoo/odoo.conf
   Restart=on-failure

   [Install]
   WantedBy=multi-user.target
   ```

   ![Crear servicio](../assets/img/08-servicio_systemd/paso01_crear-servicio.png "Crear servicio")

2. Recarga y arranca:

   ```bash
   sudo systemctl daemon-reload
   sudo systemctl enable --now odoo
   sudo systemctl status odoo
   ```

   ![Recargar y arrancar](../assets/img/08-servicio_systemd/paso02_recargar-arrancar.png "Recargar y arrancar")
