# postgres-database-setup

# Postgres database setup
    amazon-linux-extras install postgresql10 vim epel -y
    yum install -y postgresql-server postgresql-devel
    /usr/bin/postgresql-setup --initdb
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
