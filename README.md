# Android_Session11_Assignment1
Database CRUD Concept
Problem Statement

1.What is the use of SQLite open helper class inSQLite?

A helper class to manage database creation and version management.
You create a subclass implementing onCreate(SQLiteDatabase), onUpgrade(SQLiteDatabase, int, int) and optionally onOpen(SQLiteDatabase), and this class takes care of opening the database if it exists, creating it if it does not, and upgrading it as necessary. Transactions are used to make sure the database is always in a sensible state.

This class makes it easy for ContentProvider implementations to defer opening and upgrading the database until first use, to avoid blocking application startup with long-running database upgrades.

2.What is the use of OnUpgrade function in SQLiteOpenHelper class?

onUpgrade is basically for handling new db changes(could be new columns addition,table addition) for any new version of our app.

Droping the table is not always necessary in onUpgrade it all depends on what our use case is. If the requirment is to not to persists the data from our older version of app then drop should help,but if its like changing schema then it should only have alter scripts.

3.How to show SQLite database table information in Android application? what is the best
way to do it?

Table layout with cursor is the best way to show the SQLite database table information in Android application.

Showing Database information will be better suited with table layout. Since table layout is not an adapter view, We can't use the cursor adapter with it.

