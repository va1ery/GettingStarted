Hello World with Hibernate
###########################################################################


Requirements
---------------------------------------------------------------------------

- JDK 5.0 (JDK 1.4 supported but not tested) on any operating system
- Ant 1.6


Building and running the example
---------------------------------------------------------------------------

The following Ant targets are available:

    clean         Clean the build directory
    startdb       Run HSQL database server with clean DB
    schemaexport  Exports a generated schema to DB and file
    dbmanager     Start HSQL DB manager
    run           Build and run HelloWorld

1. Open your command shell and change to the example directory

2. Use ant startdb to start a fresh HSQL database, keep the database running

3. Open a second command shell and change to the example directory

4. Use ant schemaexport to export a database schema automatically to the database. Ignore any
   errors about failing ALTER TABLE statements, they are thrown because there are no tables when
   you run this for the first time.

5. Check the DDL that was also exported to the file helloworld-ddl.sql

6. Run the example with ant run and read the log output on the console

7. Reduce/increase the log output by tweaking src/java/log4j.properties and
   src/java/hibernate.cfg.xml

8. Call ant run again

9. Use ant dbmanager to open the HSQL database browser

10. If you call  again, all tables will be re-created


Notes
---------------------------------------------------------------------------

Note: You can always reset the database by restarting the database server.

Note for IntelliJ IDEA users: Open the project file in the Getting Started root directory.