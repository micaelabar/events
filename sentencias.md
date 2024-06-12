# Base de datos de EVENTS 
## 1. Obtener la edad promedio de los miembros:
 - Sentencia:
```
SELECT AVG(TIMESTAMPDIFF(YEAR, birth_date, CURDATE())) AS average_age
FROM members;
);
````
-Captura.
<imag!![Captura de pantalla 2024-06-11 211548](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/a084d4c8-9d31-4f20-9051-9789d560e816)
## 2. Obtener la edad mínima de los miembros:
 - Sentencia:
```
SELECT MIN(age) AS minimum_age
FROM members;
````
-Captura.
<imag!![Captura de pantalla 2024-06-11 211733](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/faccf679-220c-4726-a433-b85ac7b154b5)
## 3. Obtener el número total de registros asistidos:
 - Sentencia:
```
SELECT COUNT(*) AS total_registrations
FROM registrations;
````
-Captura.
<imag!![image](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/b4ddad11-a5f9-48cd-944e-25fd718d8e5f)

## 4. Obtener el número total de asistentes a todas las conferencias:
 - Sentencia:
```
SELECT SUM(attendees) AS total_attendees
FROM conferences;
````
-Captura.
<imag!![image](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/3c75ef88-aef6-421f-8add-939cf68206d5)
## 5. Obtener el número total de eventos por cada ciudad:
 - Sentencia:
```
SELECT city, COUNT(*) AS total_events
FROM events
GROUP BY city;
````
-Captura.
<imag!![image](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/0b6aff4e-3803-4328-bf8a-6a174d2da8e8)
## 6. Obtener el número de registros por cada miembro:
 - Sentencia:
```
SELECT member_id, COUNT(*) AS registration_count
FROM registrations
GROUP BY member_id;
````
-Captura.
<imag!![image](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/4da7c4d7-f1a6-4eab-b3f8-a919996f8c38)
## 7. Obtener el número de registros por cada conferencia:
 - Sentencia:
```
SELECT conference_id, COUNT(*) AS registration_count
FROM registrations
GROUP BY conference_id;
````
-Captura.
<imag!![image](https://github.com/micaelabar/Funciones-agregaci-n/assets/148156209/12aa1119-8678-4066-8813-88672a92cd71)

