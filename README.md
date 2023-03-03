# solution-for-lesson-37

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
)

CREATE TABLE "Teachers" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    subject        varchar(30)         not null,
    is_active      boolean default true,
    region_id      integer,
    group_id       integer
)

CREATE TABLE "Staff" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    is_active      boolean default true,
    region_id      integer,
    salary         integer
)

CREATE TABLE "Groups" (
    id serial,
    group_name     varchar(100)        not null,
    subject        varchar(30)         not null,
    teacher_id     integer
)

CREATE TABLE "Regions" (
    id serial,
    region_name    varchar(200)        not null
)

CREATE TABLE "Departments" (
    id serial,
    department_name varchar(200)        not null
)

```
![image](https://user-images.githubusercontent.com/81769242/222667319-31573a55-061e-45a1-b8f3-29547cfe0437.png)
![image](https://user-images.githubusercontent.com/81769242/222667376-21f7a796-0642-46bf-8c5e-c8e91ca9d693.png)

