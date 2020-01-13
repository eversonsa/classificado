# classificado
#script para gerar banco de dados

CREATE DATABASE classificados;

CREATE TABLE `classificados`.`usuarios` 
( `id` INT NOT NULL AUTO_INCREMENT ,
 `nome` VARCHAR(100) NOT NULL ,
 `email` VARCHAR(100) NOT NULL ,
 `senha` VARCHAR(32) NOT NULL ,
 `telefone` VARCHAR(30) NOT NULL ,
 PRIMARY KEY (`id`)
 ) ENGINE = InnoDB;
 
 
 CREATE TABLE `classificados`.`categorias`
 ( `id` INT NOT NULL AUTO_INCREMENT ,
 `nome` VARCHAR(100) NOT NULL ,
 PRIMARY KEY (`id`)
 ) ENGINE = InnoDB;
 
 CREATE TABLE `classificados`.`anuncios`
 ( `id` INT NOT NULL AUTO_INCREMENT ,
 `id_usuario` INT NOT NULL ,
 `id_categoria` INT NOT NULL , 
 `titulo` VARCHAR(100) NOT NULL ,
 `descricao` TEXT NOT NULL ,
 `valor` FLOAT NOT NULL ,
 `estado` INT NOT NULL ,
 PRIMARY KEY (`id`)) ENGINE = InnoDB;
