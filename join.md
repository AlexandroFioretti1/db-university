# QUERY CON JOIN

##

1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
   SELECT `students`.`name`, `surname`
   FROM students
   JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
   WHERE `degrees`.`name` = 'Corso di laurea in economia' ;

##

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

SELECT `degrees`.`name`, `degrees`.`level`, `degrees`.`address`, `departments`.`name`
FROM degrees
JOIN departments ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = 'magistrale' AND `departments`.`name` = 'Dipartimento di Neuroscienze';

##

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT `courses`.`name`, `courses`.`description`, `courses`.`period`, `courses`.`year`, `courses`.`cfu`
FROM course_teacher
JOIN courses ON `course_teacher`.`course_id` = courses.id
JOIN teachers ON `course_teacher`.`teacher_id` = teachers.id
WHERE `teachers`.`name` = 'Fulvio' AND `teachers`.`surname` = 'Amato';

##

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il
   relativo dipartimento, in ordine alfabetico per cognome e nome.

SELECT `students`.`surname`, `students`.`name`, `students`.`registration_number`, `degrees`.`name`, `degrees`.`level`, `degrees`.`address`, `departments`.`name` 
FROM students 
JOIN degrees ON `students`.`degree_id`= degrees.id 
JOIN departments ON `degrees`.`department_id` = departments.id 
ORDER BY `students`.`surname` AND `students`.`name`;
##

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

##

6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

##

7. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per superare ciascuno dei suoi esami.

#####
