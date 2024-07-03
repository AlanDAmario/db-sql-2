1. Contare quanti iscritti ci sono stati ogni anno

SELECT
    YEAR(`enrollment_date`) AS year,
    COUNT(`id`) AS total_enrollments
FROM
    `students`
GROUP BY
    YEAR(`enrollment_date`)
ORDER BY
    year;



2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT
     `office_address`,
     COUNT(`id`) AS `number_teacher`

FROM 
     `teachers`
     GROUP BY 
     `office_address`





3. Calcolare la media dei voti di ogni appello d'esame

SELECT
    `exam_id`,
    AVG(`grade`) AS average_grade
FROM
    `exam_student`
GROUP BY
    `exam_id`
ORDER BY
    `exam_id`;
4. Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT
    `departments`,
    COUNT(`id`) AS total_courses
FROM
    `degrees`
GROUP BY
    `departments`
ORDER BY
    `departments`;