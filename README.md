# zabbix_vertica_cluster_template
===================

Vertica Cluster Template for Zabbix

This template monitors the cluster as a whole, you should use it in conjunction with the per node monitoring

1. install vertica-python (https://github.com/uber/vertica-python) - using pip: "pip install --pre pytz" and than "pip install vertica-python"
2. place the script "vertica_stats.py" at the zabbix-server externalscripts folder (https://www.zabbix.com/documentation/2.0/manual/config/items/itemtypes/external), make sure it has execute permission (Ubuntu - /usr/share/zabbix/externalscripts). 
3. Import the template "Template_App_Vertica_Cluster.xml".
4. Attach the above template to the relevant hosts. The zabbix host name must match the vertica cluster host name
5. enter you db credentials in the hosts's macro section   {$VERTICA_USER_NAME},  {$VERTICA_PASSWORD} ,  {$VERTICA_DATABASE} 
