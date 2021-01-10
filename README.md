# postgres-database-setup

# Postgres database setup
    amazon-linux-extras install postgresql10 vim epel -y
    yum install -y postgresql-server postgresql-devel
    /usr/bin/postgresql-setup --initdb
# Open /var/lib/pgsql/data/pg_hba.conf file and change as shown below
    vi /var/lib/pgsql/data/pg_hba.conf
  ![image](https://user-images.githubusercontent.com/58024415/104118376-99557080-534e-11eb-97ea-072f109115f8.png)
# Enable postgres service
    systemctl enable postgresql
# Start postgres service
    systemctl start postgresql
# Change to postgres user
    su - postgres
# Connect to postgres user
    psql
# List of databases
    \l
# Connect to postgres database
    \c postgres
# Create user
    create user naresh with encrypted password 'Naresh#240';
# Provide permission to a user
    grant all privileges on database postgres to naresh;
# exit from database
    \q
# Exit from postgres user
    exit
