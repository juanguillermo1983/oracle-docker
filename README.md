# oracle-docker

1. completa las credenciales en el archivo .env junto al docker-compose.yml
2. Para iniciar el compose

```
docker compose --env-file .env up -d
```

3. copia los archivos al contenedor 
   ```
   docker cp .\human_resources\ oracle-xe:/opt/oracle
   ```
4. ingresa al contenedor de docker

   ```
   docker exec -it <container name> bash

   docker exec -it oracle-xe bash
   ```

   
5. Ingresa con sqlplus

   ```
   sqlplus sys/Maitenes2020 as sysdba
   ```




6. Instala la base de datos HR

    ```
    @/opt/oracle/human_resources/hr_install.sql;
    ```


   - define una pass para hr 
   - tablespace solo presiona enter 

7. Conecta desde Sql developer 

- Port: 1521
- Service name: FREEPDB1
- Database App User: my_user_definido_env

