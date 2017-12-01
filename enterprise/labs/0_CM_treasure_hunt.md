# Treasure Hunt

## What is ubertask optimization?

```
Permite correr los mappers y reducers en el mismo proceso como un Application Master, esto sirve para ejecuciones de programas pequeños pues reduce el tiempo que un proceso que no tiene esta optimización requiere para pasar de la fase de map a la de reduce.
```
## Where in CM is the Kerberos Security Realm value displayed?
```
- En la barra de opciones ir a Administration -> Settings 
- En los filtros escoger en la parte de Categoría Kerberos
- En los resultados buscar Kerberos Security Realm
default_realm, en ese campo se puede visualizar el realm de Kerberos.
```
## Which CDH service(s) host a property for enabling Kerberos authentication?
```
Todos los servicios como HDFS, YARN, Hive, Hue y Zookeeper llevan una propiedad que permite habilitar y deshabilitar Kerberos como metodo de autenticación.

```
## How do you upgrade the CM agents?
```
- En RHEL o similares, en el servidor que contiene los servicios de cloudera manager server buscar y actualizar el /etc/yum.repos.d/cloudera-manager.repo para que apunte a la version de CM a la que desea hacer la actualización.

En la página del Cloudera Manager
- En la barra superior desplegar el menú Hosts -> All Hosts.
- En la parte superior al listado de Hosts dar Re-run Upgrade Wizard.
- Escoger la opcion Si, actualizar los paquetes CM Agents ahora y Continuar.
- Si se actualizó el /etc/yum.repos.d/cloudera-manager.repo escoger el Matched Release.. . Caso contrario, si se tiene un repositorio personalizado escoger la opción custom repository y continuar.
- Si desea instale JDK1.7 en los hosts y el JCE Policy Files y continuar.
- Ingresar las credenciales para actualizar los agentes y continuar.
- Inicia la instalación y finalmente corrre el Host Inspector y finalizar.

Más información en https://www.cloudera.com/documentation/enterprise/5-12-x/topics/cm_ag_ug_cm5.html#concept_gs4_bsg_xw
```
## Give the tsquery statement used to chart Hue's CPU utilization?
```
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME
Donde  $SERVICENAME = hue  $CLUSTERID = 2  
```
## Name all the roles that make up the Hive service
```
- Hive Metastore Server
- WebHCat Server
- HiveServer2
- Gateway
```
## What steps must be completed before integrating Cloudera Manager with Kerberos?
```
En caso se use MIT KDC como servidor de Kerberos
- Instalar los paquetes krb5-workstation, krb5-server y openldap-client en el servidor donde se instalará el servidor KDC
- Instalar los paquetes krb5-workstation y openldap-client en los demas hosts.
- Configurar el servidor KDC y iniciar los servicios krb5kdc y kadmin.
- Asegurarse que los tickets sean renovables.
- Crear una cuenta con los permisos de crear otras cuentas en el KDC para el uso exclusivo de Cloudera Manager.

Para LDAP usar
https://www.cloudera.com/documentation/enterprise/5-11-x/topics/cm_sg_external_auth.html
```