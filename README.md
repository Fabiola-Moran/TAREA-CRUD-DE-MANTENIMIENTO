# TAREA-CRUD-DE-MANTENIMIENTO

Ejercicio en python con conexion a base de datos MySQL 

Integrantes:

MORÁN NUGRA FABIOLA YOMIRA

LÓPEZ ROMERO ALAN ARIEL

IDROVO CAMPOVERDE JHON ALFREDO

# Script Base de datos
CREAR BASE DE DATOS SI NO EXISTE plancuentas/ *! 40100 JUEGO DE CARACTERES POR DEFECTO utf8mb4 * /; USO plancuentas;

CREAR TABLA SI NO EXISTE grupo( idint (11) NO NULL AUTO_INCREMENT, descripcionvarchar (50) DEFAULT NULL, PRIMARY KEY ( id));

CREAR TABLA SI NO EXISTE plancuenta( idint (11) NO NULL AUTO_INCREMENT, codigovarchar (50) DEFAULT NULL, grupoint (11) DEFAULT NULL, descripcionvarchar (50) DEFAULT NULL, naturalezavarchar (50) DEFAULT NULL, estadoint (11) DEFAULT NULL, PRIMARY CLAVE ( id), CLAVE grupo( grupo), FK_plancuenta_grupoLLAVE EXTRANJERA RESTRICCIÓN ( grupo) REFERENCIAS grupo( id));

INSERTAR EN LOS VALORES DEL GRUPO (descripcion) ('Cta Corriente');

INSERTAR EN LOS VALORES DEL GRUPO (descripcion) ('Cta Ahorros');

INSERTAR EN PlanCuenta (codigo, grupo, descripcion, naturaleza, estado) VALORES ('1', 1, 'Cuenta familiar', 'D', VERDADERO);

INSERTAR EN PLANCuenta (codigo, grupo, descripcion, naturaleza, estado) VALUES ('2', 1, 'Cuenta empresarial', 'D', TRUE);

INSERTAR EN PlanCuenta (codigo, grupo, descripcion, naturaleza, estado) VALORES ('3', 2, 'Cuenta', 'A', VERDADERO);
