# Ejercicio
Configurar SonarQube utilizando Docker Compose, para esto necesitas dos servicios:
- Servicio: SonarQube
- Desde el host es necesario acceder a SonarQube por lo que necesitas mapear el puerto correspondiente.
- Servicio: PostgreSQL (existen otras opciones: Microsoft SQL Server, Oracle)
- Coloca un healtcheck para cada uno de los servicios.
- Los dos servicios deben pertenecer a una red de tipo bridge
- Investiga cuáles son los volúmenes necesarios para cada servicio
- Investiga cuáles son las variables de entorno para que los servicios funcionen de manera adecuada.

Volúmenes

- PostgreSQL: /var/lib/postgresql/data
- SonarQube: /opt/sonarqube/data, /opt/sonarqube/extensions, /opt/sonarqube/logs

Variables de entorno

- DB: POSTGRES_USER, POSTGRES_PASSWORD, POSTGRES_DB
- SonarQube: SONAR_JDBC_URL, SONAR_JDBC_USERNAME, SONAR_JDBC_PASSWORD

Puertos
- SonarQube expone 9000; mapeado como 9000:9000 para acceso desde el host.


# Una vez creado tu archivo .yaml realiza la respectiva prueba 
# COMPLETAR CON UNA CAPTURA DE PANTALLA LUEGO DE EJECUTAR EL ARCHIVO
<img width="1303" height="65" alt="image" src="https://github.com/user-attachments/assets/5f2a69ce-927b-43a1-b723-7b9422958829" />

# ACCEDER A LOCALHOST:puertoDefinido para ingresar a SonarQube
http://localhost:9000
<img width="1073" height="469" alt="image" src="https://github.com/user-attachments/assets/283c3db3-9475-4c29-9d0a-6a19dc2a17e5" />
<img width="1768" height="948" alt="image" src="https://github.com/user-attachments/assets/dd518cc2-a2f8-4459-830d-fe297e5bc4b1" />
