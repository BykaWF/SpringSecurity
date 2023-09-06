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