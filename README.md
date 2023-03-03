```sql
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
```
## Departments
![image](https://user-images.githubusercontent.com/81769242/222697534-3200b24a-0995-454d-ab95-f19c91580a32.png)

## Groups
![image](https://user-images.githubusercontent.com/81769242/222697622-3fdcb55b-0050-4fca-9252-e6c795e9b38e.png)

## Regions
![image](https://user-images.githubusercontent.com/81769242/222697713-70e6b907-64fe-4b4d-a538-3ada47c81cf0.png)

## Staff
![image](https://user-images.githubusercontent.com/81769242/222697796-e0775b4f-3e35-4f4f-8d8a-dea0920f4e12.png)

## Subjects
![image](https://user-images.githubusercontent.com/81769242/222697888-07d4f609-8847-4c65-ae67-ad7d8d4ad3ed.png)

## Teachers
![image](https://user-images.githubusercontent.com/81769242/222697944-b7df904d-a017-4a49-875e-06e2a5e5f5ab.png)


