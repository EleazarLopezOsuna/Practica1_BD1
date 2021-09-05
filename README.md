# Practica1_BD1

## Marco Teorico

### Modelo Conceptual

> Un modelo conceptual de datos identifica las relaciones de más alto nivel entre las diferentes entidades.
>
> Las características del modelo conceptual de datos incluyen:
>
> + Incluye las entidades importantes y las relaciones entre ellas.
> + No se especifica ningún atributo.
> + No se especifica ninguna clave principal.

### Modelo Logico

> Un modelo lógico de datos es un modelo que no es específico de una base de datos que describe aspectos relacionados con las necesidades de una organización para recopilar datos y las relaciones entre estos aspectos.
>
> Un modelo lógico contiene representaciones de entidades y atributos, relaciones, identificadores exclusivos, subtipos y supertipos y restricciones entre relaciones. Un modelo lógico también puede contener objetos de modelo de dominio o referirse a uno o varios modelos de dominio o de glosario. Una vez definidas las relaciones y los objetos lógicos en un modelo lógico de datos, utilice el área de trabajo para transformar el modelo lógico en una representación física específica de la base de datos en forma de modelo físico de datos.
>
> Mediante el área de trabajo, puede crear un modelo lógico de datos a partir de una plantilla. También puede importar tipos de datos simples de un archivo de definición de esquemas XML (.xsd) en un modelo lógico de datos como tipos de dominio.

### Modelo Fisico

> Un modelo de datos físicos es un modelo específico de bases de datos que representa objetos de datos relacionales (por ejemplo, tablas, columnas, claves principales y claves externas) y sus relaciones. Un modelo de datos físicos se puede utilizar para generar sentencias DDL que, después, se pueden desplegar en un servidor de base de datos.

## Modelo Conceptual

![ModeloConceptual](https://drive.google.com/uc?export=view&id=1k_Kk9j0JIOvJ1Wu3Qhjt0Ss9UYYnsWlN)

### Explicacion de tablas

#### Fecha

> Esta tabla se utiliza para almacenar todas las fechas, ya que por cada pais se debe ingresar la misma fecha crea datos duplicados por eso decidi utilizar una tabla especifica para manejar las fechas

#### Continente

> Tabla en la cual se almacenan los continentes existentes, esta tabla necesita ser cargada antes de empezar a llenar las demas

#### Pais_Info

> Esta tabla almacena los datos estadisticos correspondientes a cada pais, estos datos tienen relacion con el desarrollo de la enfermedad.
> + population: representa la poblacion del pais
> + population_density: representa la densidad de la poblacion en el pais
> + median_age: representa la edad media en el pais
> + aged_65_older: Indicadores de desarrollo mundial del Banco Mundial basados en distribuciones por edad / sexo de la Revisión de 2017 de Perspectivas de la población mundial de las Naciones Unidas 
> + aged_70_older: Naciones Unidas, Departamento de Asuntos Económicos y Sociales, División de Población (2017), Revisión de 2017 de Perspectivas de la población mundial
> + gdp_per_capita: Indicadores de desarrollo mundial del Banco Mundial, fuente del Banco Mundial, base de datos del Programa de Comparación Internacional
> + extreme_poverty: Indicadores de desarrollo mundial del Banco Mundial, obtenidos del Grupo de Investigación sobre el Desarrollo del Banco Mundial
> + diabetes_prevalence: Indicadores de desarrollo mundial del Banco Mundial, extraídos de la Federación Internacional de Diabetes, Diabetes Atlas
> + female_smokers: Indicadores de desarrollo mundial del Banco Mundial, obtenidos de la Organización Mundial de la Salud, Repositorio de datos del Observatorio de la salud mundial
> + male_smokers: Indicadores de desarrollo mundial del Banco Mundial, obtenidos de la Organización Mundial de la Salud, Repositorio de datos del Observatorio de la salud mundial
> + handwashing_facilities: Indicador de lugares para lavar manos segun la División de Estadística de las Naciones Unida
> + life_expectancy: Expectativa de vida segun James C. Riley, Clio Infra, División de Población de las Naciones Unidas
> + human_development_index: Indice de desarrollo segun Programa de las Naciones Unidas para el Desarrollo (PNUD)
> + excess_mortality: Base de datos de mortalidad humana (HMD) Proyecto de fluctuaciones de la mortalidad a corto plazo y Conjunto de datos de mortalidad mundial (WMD)

#### Caso

> + total_cases: Cantidad de casos totales de covid hasta la fecha dada
> + new_cases: Nuevos casos de covid en una fecha dada
> + new_cases_smoothed: 
> + total_cases_per_million: Total de casos por millon hasta la fecha dada
> + new_cases_per_million: Nuevos casos de covid en una fecha dada
> + new_cases_smoothed_per_million: 

#### Muerte

> + total_deaths: Total de muertes por covid hasta una fecha dada
> + new_deaths: Nuevas muertes por covid en una fecha dada
> + new_deaths_smoothed: 
> + total_deaths_per_million: Total de muertes por covid por millon hasta la fecha dada 
> + new_deaths_per_million: Nuevas muertes por covid en una fecha dada
> + new_deaths_smoothed_per_million: 

#### Rate

> + reproduction_rate: tasa de reproduccion segun Arroyo Marioli et al. (2020). https://doi.org/10.2139/ssrn.3581633
> + positive_rate: tasa de casos positivos
> + cardiovasc_death_rate: tasa de muerte por problemas cardiovasculares

#### Icu

> + icu_patients: Pacientes en cuidados intensivos hasta la fecha dada
> + icu_patients_per_million: Pacientes en cuidados intensivos por millon
> + weekly_icu_admissions: Pacientes en cuidados intensivos en cierta semana
> + weekly_icu_admissions_per_million: Pacientes en cuidados intensivos en cierta semana por millon

#### Info_Hospital

> + hosp_patients: Pacientes hospitalizados hasta una fecha dada
> + hosp_patients_per_million: Pacientes hospitalizados por millon
> + weekly_hosp_admissions: Admisiones semanales
> + weekly_hosp_admissions_per_million: Adminisiones semnales por millon
> + hospital_beds_per_thousand: Camas en hospitales por cada mil habitantes

#### Test

> + new_tests: Test nuevos en una fecha dada
> + total_tests: Test totales en una fecha dada
> + total_tests_per_thousand: Test totales por cada mil habitantes
> + new_tests_per_thousand: Test nuevos por cada mil habitantes
> + new_tests_smoothed: 
> + new_tests_smoothed_per_thousand: 
> + tests_per_case: Test por cada caso positivo
> + tests_units: Cantidad de test

#### Vacuna

> + total_vaccinations: Cantidad de vacunados
> + people_vaccinated: Cantidad de vacunados
> + people_fully_vaccinated: Cantidad de personas con dosis completas
> + new_vaccinations: Nuevas vacunas en una fecha dada
> + new_vaccinations_smoothed: 
> + total_vaccinations_per_hundred: Total de vacunaciones por ciento
> + people_vaccinated_per_hundred: Personas vacunadas por ciento
> + people_fully_vaccinated_per_hundred: Personas con dosis completas por ciento
> + new_vaccinations_smoothed_per_million: 
> + stringency_index: tasa de rigorosidad

## Modelo Logico

| Fecha       |           |           |
| ----------- | --------- | --------- |
| Columnas    | Id\_fecha | Date |
| Restriccion | PK        | NN |
|             | 1         | 2/24/2020 |
|             | 2         | 5/19/2021 |
|             | 3         | 12/15/2020 |
|             | 4         | 9/4/2020 |
|             | 5         | 6/15/2021 |
|             | 6         | 4/1/2021 |
|             | 7         | 4/25/2021 |
|             | 8         | 11/23/2020 |
|             | 9         | 6/30/2020 |
|             | 10        | 3/29/2020 |

| Pais        |          |          |          |
| ----------- | -------- | -------- | -------- |
| Columnas    | Id\_pais | Iso\_code | nombre |
| Restriccion | PK       | NN | NN |
|             | 1        | AFG | Afghanistan |
|             | 2        | AGO | Angola |
|             | 3        | ATG | Antigua and Barbuda |
|             | 4        | CPV | Cape Verde |
|             | 5        | CYP | Cyprus |
|             | 6        | ECU | Ecuador |
|             | 7        | GAB | Gabon |
|             | 8        | IRN | Iran |
|             | 9        | KWT | Kuwait |
|             | 10       | MCO | Monaco |

| Continente  |                |                |
| ----------- | -------------- | -------------- |
| Columnas    | Id\_continente | Nombre |
| Restriccion | PK             | NN |
|             | 1              | Asia |
|             | 2              | Africa |
|             | 3              | North America |
|             | 4              | Europe |
|             | 5              | South America |

| Pais\_Info  |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | Id\_pais | Id\_continente | population | population\_density | median\_age | aged\_65\_older | aged\_70\_older | gdp\_per\_capita | extreme\_poverty | diabetes\_prevalence | female\_smokers | male\_smokers | handwashing\_facilities | life\_expectancy | human\_development\_index | excess\_mortality |
| Restriccion | PK FK    | PK FK | NN | NN |  |  |  |  |  |  |  |  |  | NN |  |  |
|             | 1        | 1 | 39835428 | 54.422 | 18.6 | 2.581 | 1.337 | 1803.987 |  | 9.59 |  |  | 37.746 | 64.83 | 0.511 |  |
|             | 2        | 2 | 33933611 | 23.89 | 16.8 | 2.405 | 1.362 | 5819.495 |  | 3.94 |  |  | 26.664 | 61.15 | 0.581 |  |
|             | 3        | 3 | 98728 | 231.845 | 32.1 | 6.933 | 4.631 | 21490.943 |  | 13.17 |  |  |  | 77.02 | 0.778 |  |
|             | 4        | 2 | 561901 | 135.58 | 25.7 | 4.46 | 3.437 | 6222.554 |  | 2.42 | 2.1 | 16.5 |  | 72.98 | 0.665 |  |
|             | 5        | 4 | 888005 | 127.657 | 37.3 | 13.416 | 8.563 | 32415.132 |  | 9.24 | 19.6 | 52.7 |  | 80.98 | 0.887 |  |

| Caso        |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | Id\_caso | Id\_pais | Id\_fecha | total\_cases | new\_cases | new\_cases\_s | total\_cases\_pm | new\_cases\_pm | new\_cases\_s\_pm |
| Restriccion | PK       | FK | FK | NN | NN |  | NN | NN |  |
|             | 1        | 1 | 1 | 1 | 1 |  | 0.025 | 0.025 |  |
|             | 2        | 2 | 2 | 31438 | 393 | 290.429 | 926.456 | 11.581 | 8.559 |
|             | 3        | 3 | 3 | 148 | 0 | 0.286 | 1499.068 | 0 | 2.894 |
|             | 4        | 4 | 4 | 4200 | 75 | 65 | 7474.626 | 133.475 | 115.679 |
|             | 5        | 5 | 5 | 73311 | 64 | 56 | 82556.968 | 72.072 | 63.063 |

| Muerte      |            |            |            |            |            |            |            |            |            |
| ----------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Columnas    | Id\_muerte | Id\_pais | Id\_fecha | total\_deaths | new\_deaths | new\_deaths\_s | total\_deaths\_pm | new\_deaths\_pm | new\_deaths\_s\_pm |
| Restriccion | PK         | FK | FK |  |  |  |  |  |  |
|             | 1          | 1 | 1 |  |  |  |  |  |  |
|             | 2          | 2 | 2 | 696 | 11 | 7.286 | 20.511 | 0.324 | 0.215 |
|             | 3          | 3 | 3 | 5 | 0 | 0.143 | 50.644 | 0 | 1.447 |
|             | 4          | 4 | 4 | 41 | 0 | 0.429 | 72.967 | 0 | 0.763 |
|             | 5          | 5 | 5 | 374 | 0 | 1.286 | 421.169 | 0 | 1.448 |

| Rate        |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | id\_rate | Id\_pais | Id\_fecha | reproduction\_rate | positive\_rate | cardiovasc\_death\_rate |
| Restriccion | PK       | FK | FK |  |  |  |
|             | 1        | 1 | 1 |  |  | 597.029 |
|             | 2        | 2 | 2 | 1.05 |  | 276.045 |
|             | 3        | 3 | 3 | 0.68 | 0.16 | 191.511 |
|             | 4        | 4 | 4 | 1.11 | 0.001 | 182.219 |
|             | 5        | 5 | 5 | 1.07 | 0.387 | 141.171 |

| Icu         |         |         |         |         |         |         |         |
| ----------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- |
| Columnas    | id\_icu | Id\_pais | Id\_fecha | icu\_patients | icu\_patients\_per\_million | weekly\_icu\_admissions | weekly\_icu\_admissions\_per\_million |
| Restriccion | PK      | FK | FK |  |  |  |  |
|             | 1       | 1 | 1 |  |  |  |  |
|             | 2       | 2 | 2 |  |  |  |  |
|             | 3       | 3 | 3 |  |  |  |  |
|             | 4       | 4 | 4 |  |  |  |  |
|             | 5       | 5 | 5 | 8 | 9.009 |  |  |

| Info\_Hospital |                    |                    |                    |                    |                    |                    |                    |                    |
| -------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| Columnas       | id\_info\_hospital | Id\_pais | Id\_fecha | hosp\_patients | hosp\_patients\_pm | weekly\_hosp\_adm | weekly\_hosp\_adm\_pm | hospital\_beds\_pt |
| Restriccion    | PK                 | FK | FK |  |  |  |  |  |
|                | 1                  | 1 | 1 |  |  |  |  | 0.5 |
|                | 2                  | 2 | 2 |  |  |  |  |  |
|                | 3                  | 3 | 3 |  |  |  |  | 3.8 |
|                | 4                  | 4 | 4 |  |  |  |  | 2.1 |
|                | 5                  | 5 | 5 | 32 | 36.036 |  |  | 3.4 |

| Test        |          |          |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | id\_test | Id\_pais | Id\_fecha | new\_tests | total\_tests | total\_tests\_pt | new\_tests\_pt | new\_tests\_s | new\_tests\_s\_pt | tests\_per\_case | tests\_units |
| Restriccion | PK       | FK | FK |  |  |  |  |  |  |  |  |
|             | 1        | 1 | 1 |  |  |  |  |  |  |  |  |
|             | 2        | 2 | 2 |  |  |  |  |  |  |  |  |
|             | 3        | 3 | 3 |  |  |  |  |  |  |  |  |
|             | 4        | 4 | 4 | 515 |  |  | 0.917 | 407 | 0.724 | 6.3 | tests performed |
|             | 5        | 5 | 5 | 35729 | 7668213 | 8635.326 | 40.235 | 41841 | 47.118 | 747.2 | tests performed |

| Vacuna      |            |            |            |            |            |            |            |            |            |            |            |            |            |
| ----------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Columnas    | id\_vacuna | Id\_pais | Id\_fecha | total\_vs | people\_vd | people\_fully\_vd | new\_vs | new\_vs\_s | total\_vs\_ph | people\_vd\_ph | people\_fully\_vd\_ph | new\_vs\_s\_pm | stringency\_inde |
| Restriccion | PK         | FK | FK |  |  |  |  |  |  |  |  |  |  |
|             | 1          | 1 | 1 |  |  |  |  |  |  |  |  |  | 8.33 |
|             | 2          | 2 | 2 |  |  |  |  | 11468 |  |  |  | 338 | 33.33 |
|             | 3          | 3 | 3 |  |  |  |  |  |  |  |  |  |  |
|             | 4          | 4 | 4 |  |  |  |  |  |  |  |  |  | 68.98 |
|             | 5          | 5 | 5 | 718775 | 436280 | 282495 |  | 8102 | 80.94 | 49.13 | 31.81 | 9124 | 43.52 |


## DDL

```
CREATE TABLE Fecha(
	id_fecha INT NOT NULL IDENTITY(1, 1),
	fecha DATE NOT NULL,
	PRIMARY KEY(id_fecha)
);

CREATE TABLE Pais(
	id_pais INT NOT NULL IDENTITY(1, 1),
	iso_code CHAR(3) NOT NULL,
	nombre VARCHAR2(50) NOT NULL,
	PRIMARY KEY(id_pais)
);

CREATE TABLE Continente(
	id_continente INT NOT NULL IDENTITY(1, 1),
	nombre VARCHAR2(50) NOT NULL,
	PRIMARY KEY(id_continente)
);
	
CREATE TABLE Pais_Info(
	id_pais INT NOT NULL,
	id_continente INT NOT NULL,
	population BIGINT,
	population_density DECIMAL,
	median_age DECIMAL,
	aged_65_older DECIMAL,
	aged_70_older DECIMAL,
	gdp_per_capita DECIMAL,
	extreme_poverty DECIMAL,
	diabetes_prevalence DECIMAL,
	female_smokers DECIMAL,
	male_smokers DECIMAL,
	handwashing_facilities DECIMAL,
	life_expectancy DECIMAL,
	human_development_index DECIMAL,
	excess_mortality DECIMAL,
	PRIMARY KEY (id_pais),
	CONSTRAINT fk_id_pais
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_continente 
		FOREIGN KEY (id_continente) 
		REFERENCES Continente (id_continente)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Caso(
	id_caso INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_cases BIGINT,
	new_cases BIGINT,
	new_cases_smoothed FLOAT,
	total_cases_per_million FLOAT,
	new_cases_per_million FLOAT,
	new_cases_smoothed_per_million FLOAT,
	PRIMARY KEY (id_caso),
	CONSTRAINT fk_id_pais_caso
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_caso
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Muerte(
	id_muerte INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_deaths BIGINT,
	new_deaths BIGINT,
	new_deaths_smoothed FLOAT,
	total_deaths_per_million FLOAT,
	new_deaths_per_million FLOAT,
	new_deaths_smoothed_per_million FLOAT,
	PRIMARY KEY (id_muerte),
	CONSTRAINT fk_id_pais_muerte
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_muerte
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Rate(
	id_rate INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	reproduction_rate FLOAT,
	positive_rate FLOAT,
	cardiovasc_death_rate FLOAT,
	PRIMARY KEY (id_rate),
	CONSTRAINT fk_id_pais_rate
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_rate
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Icu(
	id_icu INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	icu_patients BIGINT,
	icu_patients_per_million FLOAT,
	weekly_icu_admissions FLOAT,
	weekly_icu_admissions_per_million FLOAT,
	PRIMARY KEY (id_icu),
	CONSTRAINT fk_id_pais_icu
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_icu
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Info_Hospital(
	id_info_hospital INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	hosp_patients BIGINT,
	hosp_patients_per_million FLOAT,
	weekly_hosp_admissions FLOAT,
	weekly_hosp_admissions_per_million FLOAT,
	hospital_beds_per_thousand FLOAT,
	PRIMARY KEY (id_info_hospital),
	CONSTRAINT fk_id_pais_info_hospital
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_info_hospital
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Test(
	id_test INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	new_tests BIGINT,
	total_tests BIGINT,
	total_tests_per_thousand FLOAT,
	new_tests_per_thousand FLOAT,
	new_tests_smoothed FLOAT,
	new_tests_smoothed_per_thousand FLOAT,
	tests_per_case FLOAT,
	tests_units VARCHAR(255),
	PRIMARY KEY (id_test),
	CONSTRAINT fk_id_pais_test
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_test
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Vacuna(
	id_vacuna INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_vaccinations BIGINT,
	people_vaccinated BIGINT,
	people_fully_vaccinated BIGINT,
	new_vaccinations BIGINT,
	new_vaccinations_smoothed FLOAT,
	total_vaccinations_per_hundred FLOAT,
	people_vaccinated_per_hundred FLOAT,
	people_fully_vaccinated_per_hundred FLOAT,
	new_vaccinations_smoothed_per_million FLOAT,
	stringency_index FLOAT,
	PRIMARY KEY (id_vacuna),
	CONSTRAINT fk_id_pais_vacuna
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_vacuna
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);
```

## DML

```
INSERT INTO Fecha(date) VALUES('2/24/2020');
INSERT INTO Fecha(date) VALUES('5/19/2021');
INSERT INTO Fecha(date) VALUES('12/15/2020');
INSERT INTO Fecha(date) VALUES('9/4/2020');
INSERT INTO Fecha(date) VALUES('6/15/2021');
INSERT INTO Fecha(date) VALUES('4/1/2021');
INSERT INTO Fecha(date) VALUES('4/25/2021');
INSERT INTO Fecha(date) VALUES('11/23/2020');
INSERT INTO Fecha(date) VALUES('6/30/2020');
INSERT INTO Fecha(date) VALUES('3/29/2020');

INSERT INTO Pais(iso_code, nombre) VALUES('AFG', 'Afghanistan');
INSERT INTO Pais(iso_code, nombre) VALUES('AGO', 'Angola');
INSERT INTO Pais(iso_code, nombre) VALUES('ATG', 'Antigua and Barbuda');
INSERT INTO Pais(iso_code, nombre) VALUES('CPV', 'Cape Verde');
INSERT INTO Pais(iso_code, nombre) VALUES('CYP', 'Cyprus');
INSERT INTO Pais(iso_code, nombre) VALUES('ECU', 'Ecuador');
INSERT INTO Pais(iso_code, nombre) VALUES('GAB', 'Gabon');
INSERT INTO Pais(iso_code, nombre) VALUES('IRN', 'Iran');
INSERT INTO Pais(iso_code, nombre) VALUES('KWT', 'Kuwait');
INSERT INTO Pais(iso_code, nombre) VALUES('MCO', 'Monaco');

INSERT INTO Continente(nombre) VALUES('Asia');
INSERT INTO Continente(nombre) VALUES('Africa');
INSERT INTO Continente(nombre) VALUES('North America');
INSERT INTO Continente(nombre) VALUES('Europe');
INSERT INTO Continente(nombre) VALUES('South America');

INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, handwashing_facilities, life_expectancy, human_development_index) VALUES(1, 1, 39835428, 54.422, 18.6, 2.581, 1.337, 1803.987, 9.59, 37.746, 64.83, 0.511);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, handwashing_facilities, life_expectancy, human_development_index) VALUES(2, 2, 33933611, 23.89, 16.8, 2.405, 1.362, 5819.495, 3.94, 26.664, 61.15, 0.581);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, life_expectancy, human_development_index) VALUES(3, 3, 98728, 231.845	32.1, 6.933, 4.631, 21490.943, 13.17, 77.02, 0.778);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, female_smokers, male_smokers, life_expectancy, human_development_index) VALUES(4, 2, 561901, 135.58, 25.7, 4.46, 3.437, 6222.554, 2.42, 2.1, 16.5, 72.98, 0.665);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, female_smokers, male_smokers, life_expectancy, human_development_index) VALUES(5, 4, 888005	127.657	37.3, 13.416, 8.563, 32415.132, 9.24, 19.6, 52.7, 80.98, 0.887);

INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, total_cases_per_million, new_cases_per_million) VALUES(1, 1, 1, 1, 0.025, 0.025);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(2, 2, 31438, 393, 290.429, 926.456, 11.581, 8.559);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(3, 3, 148, 0, 0.286, 1499.068, 0, 2.894);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(4, 4, 4200, 75, 65, 7474.626, 133.475, 115.679);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(5, 5, 73311, 64, 56, 82556.968, 72.072, 63.063);

INSERT INTO Muerte(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(2, 2, 696, 11, 7.286, 20.511, 0.324, 0.215);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(3, 3, 5, 0, 0.143, 50.644, 0, 1.447);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(4, 4, 41, 0, 0.429, 72.967, 0, 0.763);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(5, 5, 374, 0, 1.286, 421.169, 0, 1.448);

INSERT INTO Rate(id_pais, id_fecha, cardiovasc_death_rate) VALUES(1, 1, 597.029);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, cardiovasc_death_rate) VALUES(2, 2, 1.05, 276.045);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(3, 3, 0.68, 0.16, 191.511);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(4, 4, 1.11, 0.001, 182.219);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(5, 5, 1.07, 0.387, 141.171);

INSERT INTO Icu(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Icu(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Icu(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Icu(id_pais, id_fecha) VALUES(4, 4);
INSERT INTO Icu(id_pais, id_fecha, icu_patients, icu_patients_per_million) VALUES(5, 5, 8, 9.009);

INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(1, 1, 0.5);
INSERT INTO Info_Hospital(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(3, 3, 3.8);
INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(4, 4, 2.1);
INSERT INTO Info_Hospital(id_pais, id_fecha, hosp_patients, hosp_patients_per_million, hospital_beds_per_thousand) VALUES(5, 5, 32, 36.036, 3.4);

INSERT INTO Test(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Test(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Test(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Test(id_pais, id_fecha, new_tests, new_tests_per_thousand, new_tests_smoothed, tests_per_case, tests_units) VALUES(4, 4, 515, , 0.917, 407, 0.724, 6.3, tests performed);
INSERT INTO Test(id_pais, id_fecha, new_tests, total_tests, total_tests_per_thousand, new_tests_per_thousand, new_tests_smoothed, tests_per_case, tests_units) VALUES(5, 5, 35729, 7668213, 8635.326, 40.235, 41841, 47.118, 747.2, tests performed);

INSERT INTO Vacuna(id_pais, id_fecha, stringency_index) VALUES(1, 1, 8.33);
INSERT INTO Vacuna(id_pais, id_fecha, new_vaccinations_smoothed, new_vaccinations_smoothed_per_million, stringency_index) VALUES(2, 2, 11468, 338, 33.33);
INSERT INTO Vacuna(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Vacuna(id_pais, id_fecha, stringency_index) VALUES(4, 4, 68.98);
INSERT INTO Vacuna(id_pais, id_fecha, total_vaccinations, people_vaccinated, people_fully_vaccinated, new_vaccinations_smoothed, total_vaccinations_per_hundred, people_vaccinated_per_hundred, people_fully_vaccinated_per_hundred, new_vaccinations_smoothed_per_million, stringency_index) VALUES(5, 5, 718775, 436280, 282495, 8102, 80.94, 49.13, 31.81, 9124, 43.52);
```

## Glosario

1. DML
> Data Manipulation Language o Lenguaje de Manipulacion de Datos
2. DDL
> Data Definition Language o Lenguaje de Definicion de Datos
3. Primary Key
> Es el atributo que identifica a un conjunto de atributos, esta llave nos sirve para poder encotrar datos con mayor facilidad y evitar duplicados
4. Foreign Key
> Una llave foranea en una tabla A hace referencia a una llave primaria de una tabla B con la cual tiene relacion
5. Relacion
> Una relacion es una conexion existente entre dos tablas
6. Modelo Fisico
> El modelo fisico son todas las instrucciones con las cuales generamos las entidades, relaciones, atributos, etc.
7. Modelo Logico
> El modelo logico es una representacion grafica de las tablas y algunos ejemplos de datos ingresados
8. Modelo Conceptual
> El modelo conceptual es lo que mejor conocemos como Entidad Relacion, en este modelo podemos observar de manera grafica las entidades y sus relaciones
9. Entidad
> Una entidad o tambien conocida como tabla es el nombre que llevan los conjuntos de datos, estas tienen atributos, relaciones, restricciones, etc.
10. Atributo
> Un atributo es una parte escencial de una entidad, este tiene un tipo de dato definido, restricciones, etc.
