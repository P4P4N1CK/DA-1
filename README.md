```
Author: Nguyen Trung Hau
Email: ken.hdpro@gmail.com
Facebook: http://fb.com/irf1404
```

# INSTALL DIRECTADMIN
<b>(*) PLEASE GO THROUGH THE CONFIGURATION STEPS BEFORE INSTALLATION [HERE](https://github.com/irf1404/DACONFIG)</b>
```
# Directadmin 1.630
wget -O setup.sh "https://raw.githubusercontent.com/irf1404/DA/master/da-1630-linux64.sh" && chmod +x setup.sh && ./setup.sh 2>&1|tee directadmin_inѕtall.log

# Directadmin 1.631
wget -O setup.sh "https://raw.githubusercontent.com/P4P4N1CK/DA-1/patch-1/da-1631-linux64.sh" && chmod +x setup.sh && ./setup.sh 2>&1|tee directadmin_inѕtall.log

# Directadmin 1.632

```

# NULL DIRECTADMIN
```
#!/bin/sh

LICENSE=/usr/local/directadmin/conf/license.key
DACONF_FILE=/usr/local/directadmin/conf/directadmin.conf

rm -rf $LICENSE
wget -O $LICENSE "https://raw.githubusercontent.com/irf1404/DACONFIG/master/license.key"

chmod 600 ${LICENSE}
chown diradmin:diradmin ${LICENSE}

if [ -s ${LICENSE} ] && [ -s ${DACONF_FILE} ]; then
	echo 'action=directadmin&value=restart' >> /usr/local/directadmin/data/task.queue.cb
	/usr/local/directadmin/dataskq --custombuild
fi

exit 0;

https://raw.githubusercontent.com/irf1404/DA/master/da-xxxx-linux64.tar.gz
```
