#
-1 Consegna: Selezionare tutti gli studenti nati nel 1990 (160)

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SHOW `students`
- SELECT \* from `students`
  WHERE YEAR(date_of_birth) = 1990;
  response = 160 `students`

##
-2 Consegna: Selezionare tutti i corsi che valgono più di 10 crediti (479)

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SELECT `cfu` FROM `courses` WHERE `cfu`>10;
- SELECT `cfu` FROM `courses` WHERE `cfu`>10;
  response = 479

###
-3 Consegna: Selezionare tutti gli studenti che hanno più di 30 anni

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SELECT \* FROM `students`
  WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) >30;
  response = 3392 students >30

####
-4 Consegna: Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SELECT \* FROM courses
  WHERE period ='I semestre' and YEAR = 1;
  response = 286

#####
-5 Consegna:Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

- SHOW `databases`
- USE `91_university`
- SELECT \* FROM exams
  WHERE DATE ="2020-06-20" AND HOUR>= "14:00:00";  
   response = 21

######
-6 Consegna:Selezionare tutti i corsi di laurea magistrale (38)

- SHOW `databases`
- USE `91_university`
- SELECT \* FROM degrees
  WHERE level ="magistrale";
  response= 38

######
-7 Consegna:Da quanti dipartimenti è composta l'università? (12)

- SHOW `databases`
- USE `91_university`
- DESCRIBE departments;
- SELECT COUNT(\*) as "Departments"
  FROM departments;
  response= 12

######
-8 Consegna: Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

- SHOW `databases`
- USE `91_university`
- DESCRIBE teachers;
- SELECT \* FROM teachers
  WHERE phone is NULL;
  response= 50
