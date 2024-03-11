# API test

crud simples com uma web api .net 7 para consolidar conhecimento em APIs

## Índice

- [Visão Geral](#visão-geral)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Como Usar](#como-usar)

## Visão Geral

a finalidade deste projeto é fornecer um exemplo prático de como criar uma api rest para operações básicas de um sistema de gerenciamento de recursos, neste caso, gerenciando informações de funcionários(as).


## Tecnologias Utilizadas

- .net 7
- api rest
- entity framework core
- sql server management studio
- swagger

## Como Usar

para utilizar, você precisará criar no sgbd de sua preferência (nesse projeto utilizei o sql server) e criar um novo banco de dados usando o seguinte comando:

```bash
-- 1º
create database Employee

-- 2º
use Employee
create table Employees (
  id INT PRIMARY KEY IDENTITY(1,1),
  name NVARCHAR(100) NOT NULL,
  age INT NOT NULL,
  photo NVARCHAR(100)
);
```

também será necessário alterar a connection string na pasta "APItest.Infra.ConnectionContext.cs"
```bash
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
        => optionsBuilder.UseSqlServer("Server=seuServidor;Database=Employees; Trusted_Connection = True; TrustServerCertificate=True;");
```
