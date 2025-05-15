# odoo-on-ubuntu-restore-db   

sudo su - postgres   
createdb your_db_name   
psql your_db_name < /tmp/odoo_restore/dump.sql   
exit   
sudo mkdir -p /var/lib/odoo/.local/share/Odoo/filestore/your_db_name   
sudo cp -r /tmp/odoo_restore/filestore/* /var/lib/odoo/.local/share/Odoo/filestore/your_db_name/   
sudo chown -R odoo:odoo /var/lib/odoo/.local/share/Odoo/filestore/your_db_name   
