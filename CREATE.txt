use master
go

IF db_id ('PRUEBA_DATOS') is not null
	drop database PRUEBA_DATOS
go

--Creating Database
CREATE DATABASE PRUEBA_DATOS
on primary

(
	name= "PRUEBA_DATOS_PRI",
	filename= "F:\PRUEBA_DATOS\PRI\PRUEBA_DATOS_PRI.mdf",
	size= 12MB,
	maxsize= unlimited,
	filegrowth= 8MB
),
(
	name= "PRUEBA_DATOS_SEC",
	filename= "F:\PRUEBA_DATOS\SEC\PRUEBA_DATOS_SEC.ndf",
	size= 12MB,
	maxsize= 30MB,
	filegrowth= 10%
)
log on
(
	name= "PRUEBA_DATOS_TRA",
	filename= "F:\PRUEBA_DATOS\TRA\PRUEBA_DATOS_TRA.ldf",
	size= 15MB,
	maxsize = 90MB,
	filegrowth= 15%

)
