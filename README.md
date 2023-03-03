CREATE TABLE "Students" (
    id             serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    department_id  integer             not null,
    dob            date,
    date_joined    date,
    date_graduated date,
    is_graduated   boolean default false,
    is_active      boolean default true,
    gpa            real    default 0,
    grade          integer             not null,
    region_id      integer,
    group_id       integer
);

CREATE TABLE "Teachers" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    subject        integer             not null,
    is_active      boolean default true,
    department_id  integer,
    region_id      integer
);

CREATE TABLE "Staff" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    is_active      boolean default true,
    region_id      integer,
    department_id  integer,
    salary         integer
);

CREATE TABLE "Groups" (
    id serial,
    group_name     varchar(100)        not null,
    department_id  integer
);

CREATE TABLE "Regions" (
    id serial,
    region_name    varchar(200)        not null
);

CREATE TABLE "Departments" (
    id serial,
    department_name varchar(200)       not null
);

CREATE TABLE "Subjects" (
    id serial,
    subject_name   varchar(200)       not null
);
