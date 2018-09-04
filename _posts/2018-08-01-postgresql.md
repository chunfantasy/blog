---
layout: post
title: PostgreSQL Note
description: "This note is about the problems that I met while using PostgreSQL."
modified: 2018-08-01
tags: [Database]
comments: true
image:
  feature: 2018-08-01-postgresql.png
---

This note is about the problems that I met while using PostgreSQL.

# Install

Follow official user guide.

# Access

``` bash
// Modify pg_hba.conf
$ sudo vim /etc/postgresql/10/main/pg_hba.conf

// local all postgress trues

// Restart service
$ sudo service postgresql restart

// Connect
$ psql -U postgres
```

# Create User

``` bash
$ CREATE ROLE username WITH LOGIN PASSWORD 'password';
```

# Grant

``` bash
$ ALTER ROLE username CREATEDB;
```

# Create Database

``` bash
$ CREATE DATABASE db_name;
```
