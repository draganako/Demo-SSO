# demo-sso
An SSO server based on Spring Authorization server and a resource server.

This project is an exercise and a practical illustration to the articles 2 and 3 of **[Building SSO based on Spring Authorization Server](https://medium.com/@d.snezhinskiy/building-sso-based-on-spring-authorization-server-part-2-of-3-fc0e5db83609)** by D. Snezhinskiy. It consists of an authorization and a resource server.

The authorization server implements code grant authorization and grant password authorization, using opaque tokens. Users, roles and authorities are stored in a PostgreSQL database. Authorization using Social Login (Google) is also provided.

The resource server is configured to retrieve a list of user authorities from the authorization server, using an opaque token. There are demo endpoints defined in the resource server that are accessible only to users with certain authorities.
