# Network Architecture

The lab consists of a multi-machine virtual environment with the following components:

- **DNS Servers (ns1, ns2):** Handle domain name resolution for all clients.
- **LDAP Server:** Stores user credentials and group memberships.
- **Kerberos Server:** Provides centralized authentication and single sign-on.
- **Clients:** Request authentication and access services through Kerberos.

## Authentication Flow
1. Client requests authentication from Kerberos.
2. Kerberos verifies credentials against LDAP.
3. Kerberos issues a ticket-granting ticket (TGT).
4. Client uses TGT to access services without re-entering credentials.

