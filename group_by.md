# QUERY CON GROUP BY

1. Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(`id`) AS `total_subscribed`
FROM `students`
GROUP BY YEAR(`enrolment_date`);

##

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT COUNT(`id`) AS `same_building_works`, `office_address`
FROM `teachers`
GROUP BY `office_address`;

##

3. Calcolare la media dei voti di ogni appello d'esame

SELECT AVG(`vote`) AS `media_vote`,`exam_id`
FROM `exam_student`
GROUP BY `exam_id`;

##

4. Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT COUNT(`degrees`.`id`), `departments`.`name`
FROM degrees
JOIN departments ON `degrees`.`department_id` = `departments`.`id`
GROUP BY `degrees`.`department_id`;

##
