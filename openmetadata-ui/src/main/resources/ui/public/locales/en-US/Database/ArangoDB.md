# ArangoDB
In this section, we provide guides and references to use the ArangoDB connector. You can view the full documentation for ArangoDB <a href="https://docs.open-metadata.org/connectors/database/arango" target="_blank">here</a>.

## Requirements
To extract metadata, the user used in the connection needs to be able to perform `find` operation on collection and `listCollection` operations on database available in ArangoDB.

You can find further information on the Hive connector in the <a href="https://docs.open-metadata.org/connectors/database/arango" target="_blank">here</a>.

## Connection Details

$$section
### Username $(id="username")
Username to connect to Arangodb. This user must have access to perform `find` operation on collection and `listCollection` operations on database available in ArangoDB.
$$

$$section
### Password $(id="password")
Password to connect to ArangoDB.
$$

$$section
### Host Port $(id="hostPort")

This parameter specifies the host and port of the ArangoDB instance. This should be specified as a string in the format `hostname:port`. For example, you might set the hostPort parameter to `localhost:27017`.

If you are running the OpenMetadata ingestion in a docker and your services are hosted on the `localhost`, then use `host.docker.internal:27017` as the value.
$$

$$section
### Database Name $(id="databaseName")
In OpenMetadata, the Database Service hierarchy works as follows:
```
Database Service > Database > Schema > Table
```
In the case of ArangoDB, we won't have a Database as such. If you'd like to see your data in a database named something other than `default`, you can specify the name in this field.
$$

$$section
### Connection Options $(id="connectionOptions")
Additional connection options to build the URL that can be sent to service during the connection. The connectionOptions parameter is specific to the connection method being used. For example, if you are using SSL encryption, you might set the connectionOptions parameter to {'ssl': 'true', 'sslTrustStore': '/path/to/truststore'}.
$$
