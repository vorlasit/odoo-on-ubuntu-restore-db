# backup db postgres ubuntu server   
    root@nobrand-prod:/opt/odoo# pg_dump -U odoo -h localhost -W nobrand_prod > nobrand_backup.sql   
    and get filetore to now server

# ✅ วิธีที่: ใช้ scp คัดลอกไฟล์จาก Server มาที่ Desktop
    scp user@192.168.1.100:/home/user/data/report.pdf ~/Downloads/

# odoo-on-ubuntu-restore-db    
# allow postgres user     

    sudo chown postgres:postgres /tmp/odoo_restore/dump.sql    
    
    sudo su - postgres   
    createdb your_db_name     
    psql your_db_name < /tmp/odoo_restore/dump.sql   
    exit   
    sudo mkdir -p odoo18/.local/share/Odoo/filestore/retailed_db   
    sudo cp -r /opt/mnt/backups/filestore/retailed_db/* odoo18/.local/share/Odoo/filestore/retailed_db  
    sudo chown -R odoo18:odoo18 odoo18/.local/share/Odoo/filestore/retailed_db   
    sudo chmod -R 777 Centralize-Retail  
    sudo chmod -R 777 enterprise18    
