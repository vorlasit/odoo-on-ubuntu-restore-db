#backup db postgres ubuntu server   
root@nobrand-prod:/opt/odoo# pg_dump -U odoo -h localhost -W nobrand_prod > nobrand_backup.sql   
and get filetore to now server


# odoo-on-ubuntu-restore-db    
#allow postgres user    
root@docker:/opt/odoo15# sudo chown postgres:postgres /opt/odoo15   
root@docker:/opt/odoo15# sudo chmod -R 755 /opt/odoo15   

sudo su - postgres   
createdb your_db_name     
sudo chown postgres:postgres /tmp/odoo_restore/dump.sql    
psql your_db_name < /tmp/odoo_restore/dump.sql   
exit   
sudo mkdir -p odoo18/.local/share/Odoo/filestore/retailed_db   
sudo cp -r /opt/mnt/backups/filestore/retailed_db/* odoo18/.local/share/Odoo/filestore/retailed_db  
sudo chown -R odoo18:odoo18 odoo18/.local/share/Odoo/filestore/retailed_db   
sudo chown -R odoo18:odoo18 enterprise18  
sudo chown -R odoo18:odoo18 Centralize-Retail  
sudo chmod -R 755 Centralize-Retail  
sudo chmod -R 755 enterprise18    
