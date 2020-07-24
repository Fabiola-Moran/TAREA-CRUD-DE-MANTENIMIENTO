# TAREA-CRUD-DE-MANTENIMIENTO

Ejercicio en python con conexion a base de datos MySQL 
Integrantes:

MORÁN NUGRA FABIOLA YOMIRA

LÓPEZ ROMERO ALAN ARIEL

IDROVO CAMPOVERDE JHON ALFREDO

# Script Base de datos
CREATE DATABASE IF NOT EXISTS plancuentas /*!40100 DEFAULT CHARACTER SET utf8mb4 */;
USE plancuentas;
CREATE TABLE IF NOT EXISTS grupo (
  id int(11) NOT NULL AUTO_INCREMENT,
  descripcion varchar(50) DEFAULT NULL,
  PRIMARY KEY (id)
);

CREATE TABLE IF NOT EXISTS plancuenta (
  id int(11) NOT NULL AUTO_INCREMENT,
  codigo varchar(50) DEFAULT NULL,
  grupo int(11) DEFAULT NULL,
  descripcion varchar(50) DEFAULT NULL,
  naturaleza varchar(50) DEFAULT NULL,
  estado int(11) DEFAULT NULL,
  PRIMARY KEY (id),
  KEY grupo (grupo),
  CONSTRAINT FK_plancuenta_grupo FOREIGN KEY (grupo) REFERENCES grupo (id)
);

INSERT INTO Grupo (descripcion) VALUES('Cta Corriente'); 
INSERT INTO Grupo (descripcion) VALUES('Cta Ahorros'); 
INSERT INTO PlanCuenta(codigo,grupo,descripcion,naturaleza,estado) VALUES ('1',1,'Cuenta familiar','D',TRUE);
INSERT INTO PlanCuenta(codigo,grupo,descripcion,naturaleza,estado) VALUES ('2',1,'Cuenta empresarial','D',TRUE); 
INSERT INTO PlanCuenta(codigo,grupo,descripcion,naturaleza,estado) VALUES ('3',2,'Cuenta','A',TRUE);
