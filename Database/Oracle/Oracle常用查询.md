## Oracle常用语句

1. 查询用户所拥有角色

   ```plsql
   select * from dba_role_privs WHERE GRANTEE='<用户名>';
   ```

2. 查询特定角色所具有的的权限

   ```sql
   select * from dba_sys_privs where grantee='<角色名>'
   ```

3. 从特定用户收回特定权限

   ```plsql
   revoke <角色名> from <用户名> ;
   ```

4. 创建角色

   ```plsql
   CREATE ROLE <角色名>;
   ```

5. 给角色赋权

   ```plsql
   GRANT CREATE SESSION TO <角色名>;
   GRANT CREATE TABLE TO <角色名>;
   GRANT CREATE SYNONYM TO <角色名>;
   GRANT CREATE VIEW TO <角色名>;
   GRANT CREATE SEQUENCE TO <角色名>;
   GRANT CREATE PROCEDURE TO <角色名>;
   GRANT CREATE TRIGGER TO <角色名>;
   GRANT SELECT ANY TABLE TO <角色名>;
   GRANT UPDATE ANY TABLE TO <角色名>;
   GRANT INSERT ANY TABLE TO <角色名>;
   GRANT DELETE ANY TABLE TO <角色名>;
   ```

6. 给用户赋予角色

   ```plsql
   GRANT <ROLENAME> TO <USERNAME>;
   ```
