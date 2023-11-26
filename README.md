# apacheds-ldap-ldif-example

Example of Simple ApacheDS LDIF Files

- Begin by installing Apache Directory Studio—an integrated development environment (IDE) that comes bundled with ApacheDS, simplifying the setup process.
- Proceed to create an ApacheDS server using Apache Directory Studio and initiate its operation.
- Facilitate the population of the server by importing user data from the "test-import.ldif" file. This step ensures the presence of predefined users within the directory.

Example LDIF Structure

dc=example,dc=com
|-- ou=People
|   |-- cn=John Doe
|   |   |-- uid=jdoe
|   |   |-- userPassword: {SHA}hashed_password
|   |   |-- mail=jdoe@example.com
|   |   |-- sn=Doe
|   |   |-- givenName=John
|   |   |-- objectClass: inetOrgPerson
|   |   |-- objectClass: organizationalPerson
|   |   |-- objectClass: person
|   |   |-- objectClass: top
|   |-- cn=Jane Smith
|       |-- uid=jsmith
|       |-- userPassword: {SHA}hashed_password
|       |-- mail=jsmith@example.com
|       |-- sn=Smith
|       |-- givenName=Jane
|       |-- objectClass: inetOrgPerson
|       |-- objectClass: organizationalPerson
|       |-- objectClass: person
|       |-- objectClass: top
|
|-- ou=Groups
    |-- cn=Admins
        |-- member: cn=John Doe,ou=People,dc=example,dc=com
        |-- member: cn=Jane Smith,ou=People,dc=example,dc=com
        |-- objectClass: groupOfNames
        |-- objectClass: top
        |-- cn=Admins
