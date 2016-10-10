# sampledata_imc
Sample DB for IMC

```
	echo "Getting sample data..."
	wget -O /tmp/imc_sample_data.sql https://raw.githubusercontent.com/icos-urenio/sampledata_imc/master/imc_sample_data_no_db
	sed -i -e $sed_arg /tmp/imc_sample_data.sql

	echo "Installing sample data in $db_name..."
	mysql -u $db_user -p$db_pswd -Bse "DROP DATABASE IF EXISTS $db_name;CREATE DATABASE $db_name;USE $db_name"
	mysql -h "localhost" -u "$db_user" "-p$db_pswd" "$db_name" < "/tmp/imc_sample_data.sql"
```
