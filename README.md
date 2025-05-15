# odoo-on-ubuntu-restore-db   

sudo su - postgres   
createdb your_db_name   
psql your_db_name < /tmp/odoo_restore/dump.sql   
exit   
sudo mkdir -p odoo18/.local/share/Odoo/filestore/retailed_db   
sudo cp -r /opt/mnt/backups/filestore/retailed_db/* odoo18/.local/share/Odoo/filestore/retailed_db  
sudo chown -R odoo18:odoo18 odoo18/.local/share/Odoo/filestore/retailed_db   
sudo chown -R odoo18:odoo18 enterprise18  
sudo chown -R odoo18:odoo18 Centralize-Retail  
sudo chmod -R 755 Centralize-Retail  
sudo chmod -R 755 enterprise18    
