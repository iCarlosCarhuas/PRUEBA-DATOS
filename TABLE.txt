use PRUEBA_DATOS
go
--Creating Tables
--Primary key 
--It can't be empty (not null by default)
create table tb_libro
(
	cod_lib int not null primary key, --codigo libro
	des_lib text not null, --descripcion de producto
	fec_publicacion date not null, --fecha de publicacion
	pre_lib money not null -- precio de producto 
)
go
--modifying table; adding 
alter table tb_libro
add can_lib int not null,
	cod_autor int not null
go

--creating table
create table tb_autor
(
	cod_autor int not null,
	nom_autor varchar(30),
	ape_autor varchar(30),
	hijos_autor int,
)