# JenkinsExercise
For Jenkins exercise 

# Pre-requisitos
1. Docker
2. Organización de Azure DevOps

# Requerimiento

* Crea un proceso de CI/CD donde inicialmente tengas el codígo fuente versionado en tu organización de Azure DevOps.
* Una vez que hagas un push a la rama principal debe ejecutarse el pipeline que encola la ejecución hacia Jenkins.
* En jenkins debes hacer:
  * Checkout --> preferiblemente una aplicación java
  * SonarScanner --> sí el build es exitoso continua con el build
  * Test (Opcional)
  * Build --> puedes generar un artefacto de tu preferencia ( .jar, Imagen Docker)
  * Deploy --> ejecuta el artefecto generado en tu entorno (ya sea un API o aplicación de consola)
* En Azure DevOps en el mismo pipeline en un segundo task debes hacer :
  * Un script en bash o powershell que:
    * Numero random mayor que 10 durante 5 intentos
    * buscar dentro del directorio del repositorio el jenkins file e imprimirlo
 
# Reglas

1. Conexión de Azure a Jenkins por Services connection
2. En jenkins el pipeline debe estar en los siguientes formatos:
    1. SharedLibrary --> (https://www.jenkins.io/doc/book/pipeline/shared-libraries/)
    2. JenkinsFile --> (https://www.jenkins.io/doc/book/pipeline/jenkinsfile/)
3. El pipeline debe estar dividido por Stage / Steps
4. Opcional tareas paralelas

# Que esperamos?

1. Adjuntar el repositorio publico:
  1. Logs de ejecución
  2. Azure pipeline yaml
  3. Captura de pantalla:
     1. Services Connections
     2. Ejecución Pipeline Azure donde se vea la url de tu aplicación jenkins.
     3. Pipeline Jenkins
  4. Zip con jenkinsFile o sharedlib (usando el 2do, adjunta print de la configuración general de jenkins)
  5. Artafacto generado (Cualquiera de las dos)
     1. txt con url de imagen de docker en repositorio público
     2. zip con artefacto generado
