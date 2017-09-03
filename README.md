# Rocket Todo Example with connection pool ported to MySQL

Rocket needs rust nightly
rustup default nightly

This example makes use of a MySQL database via `diesel` to store todo tasks. As
a result, you'll need to have `MySQL` and its headers installed:


## Running

**Before running, building, or testing this example, you'll need to ensure the
following:**

  1. A MySQL database file with the proper schema is present.

     On a Unix machine or with bash installed, you can simply run the
     `boostrap.sh` script to create the database. The script installs the
     `diesel_cli` tools if they're not already installed and runs the
     migrations. The script will output a `DATABASE_URL` variable.

     You can also install the Diesel CLI and run the migrations manually with
     the following commands:

     ```
     # install Diesel CLI tools
     cargo install diesel_cli 

     # create initial db structure
     diesel migration run
     ```

  2. A `DATABASE_URL` environment variable is set that points to the MySQL
connection url


     Use the `DATABASE_URL` variable emitted from the `bootstrap.sh` script, or
     enter it manually, as follows:
     *  `DATABASE_URL=mysql://root@localhost/test2 cargo run`

  3. To listen on all interfaces add ROCKET_ENV=production env variable