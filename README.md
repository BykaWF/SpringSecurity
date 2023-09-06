# SpringSecurity


 ### There are two ways make your spring security life easy:
    1. Implement UserDetail interface ( more controle)
    2. User already peresent User class or extend it

- `UserDetail` interface stores all user information which are going to be encapsulated for Auth object

  ```
  @Enumerated(EnumType.STRING) -> tells that will enum.
  private Role role;
    ```

- `GrantedAuthority` -> tell us role of user


### 2. Create JWT Filter
We want to have active this filter when user send a request to the server

- `FilterChain filterChain` -> provide ability to make a chain of filters
- `OncePerRequestFilter` -> ensure that will be executed per request dispatch

For to be able handling request and response add:
```agsl
                <dependency>
			<groupId>io.jsonwebtoken</groupId>
			<artifactId>jjwt-api</artifactId>
			<version> 0.11.5</version>
		</dependency>

		<dependency>
			<groupId>io.jsonwebtoken</groupId>
			<artifactId>jjwt-impl</artifactId>
			<version>0.11.5</version>
		</dependency>

		<dependency>
			<groupId>io.jsonwebtoken</groupId>
			<artifactId>jjwt-jackson</artifactId>
			<version>0.11.5</version>
		</dependency>
```