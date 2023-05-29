## Solution 1
SELECT *  
FROM `students`   
WHERE YEAR(`date_of_birth`) = 1990 ;

---
## Solution 2
SELECT *   
FROM `courses`  
WHERE `cfu` > 10 ; 

---
## Solution 3
SELECT *   
FROM `students`  
WHERE  DATE_FORMAT(FROM_DAYS(DATEDIFF(NOW(),`date_of_birth`)), '%y') >= 30;  

---
## Solution 4
SELECT *   
FROM `courses`  
WHERE `period` = 'I semestre'  
AND `year` = 1;  

---
## Solution 5
FROM `exams`  
WHERE HOUR(`hour`) >= 14  
AND `date` = '2020/06/20';   

---
## Solution 6
SELECT *   
FROM `degrees`  
WHERE `level` = 'magistrale';

---
## Solution 7
SELECT COUNT(*) as 'dipartimenti'  
FROM `departments`;

---
## Solution 8
SELECT *  
FROM `teachers`  
WHERE `phone` IS NULL  

---
## BONUS 1
SELECT COUNT(*), YEAR(`enrolment_date`) AS 'anno_di_iscrizione'
FROM `students`
GROUP BY(`anno_di_iscrizione`);

---
## BONUS 2
SELECT COUNT(*) as professori, `office_address` as 'indirizzo'  
FROM `teachers`  
GROUP BY (`indirizzo`)  
HAVING `professori` <> 1  
ORDER BY `professori`;

---
## BONUS 3
