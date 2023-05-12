#
-1 Consegna: Selezionare tutti gli studenti nati nel 1990 (160)

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SHOW `students`
- SELECT * from students WHERE YEAR(date_of_birth) = 1990;
       response = 160 students
##
-2 Consegna: Selezionare tutti i corsi che valgono più di 10 crediti (479)

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SELECT `cfu` FROM `courses` WHERE `cfu`>10;
- SELECT `cfu` FROM `courses` WHERE `cfu`>10;
    response = 479 
##
-3 Consegna: Selezionare tutti gli studenti che hanno più di 30 anni

- SHOW `databases`
- USE `91_university`
- SHOW `tables`
- SELECT * FROM `students`
 WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) >30;

###