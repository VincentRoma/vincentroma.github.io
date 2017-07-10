## Sqoop For SAP

#### Regular CMD

    sqoop import --direct --connect "jdbc:sap://<IP>:<PORT>?currentschema=<SCHEMA>" --driver com.sap.db.jdbc.Driver --username <USERNAME> --password <PASSWORD> --table "<TABLE>" --target-dir "/user/cloudera/SAP" -m 1

#### OPTIONS

--check-column id --incremental lastmodified --last-value 2017-01-01

-m

--hive


## Sqoop for Oracle

#### CMD with output format

sqoop import --direct --connect "jdbc:oracle:thin:@<IP>:<PORT>/<REGION>" --username <USERNAME> --password <PASSWORD> --query 'SELECT * FROM TABLE where rownum < 1000000 and $CONDITIONS' --target-dir "/user/cloudera/ORACLE" --as-textfile --escaped-by \\ --enclosed-by '\"' -m 1

#### OPTIONS

--enclosed-by

--escaped-by

$CONDITIONS
