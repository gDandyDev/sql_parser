Вариант 1. Выражение CREATE TABLE.
1. CREATE [{GLOBAL | LOCAL} TEMPORARY] TABLE <название таблицы> (<определение элемента таблицы>[{, <определение  элемента таблицы>}...]) [ON COMMIT {DELETE | PRESERVE} ROWS]
2. <определение элемента таблицы> ::= <определение ограничений таблицы> | <определение поля>
3. <определение ограничений таблицы> ::= <ограничение уникальности> | <ссылочное ограничение>
4. <ограничение уникальности> ::= {UNIQUE | PRIMARY KEY} (<список полей>)
5. <ссылочное ограничение> ::= FOREIGN KEY (<список полей>) <спецификация ссылки>
6. <спецификация ссылки> ::= REFERENCES <название таблицы> [(<список полей>)] [ON UPDATE <действие триггера>] [ON DELETE <действие триггера>]
7. <действие триггера> ::= CASCADE | SET NULL | SET DEFAULT | NO ACTION 
8. <список полей> ::= <название поля>[{, <название поля>}...]
9. <определение поля> ::= <название поля> <тип данных> [<определение ограничений поля>...]
10. <тип данных> ::= <строковый тип данных> | <числовой тип данных> | <временной тип данных> 
11. <строковый тип данных> ::= CHAR[(<длина>)] | VARCHAR[(<длина>)]
12. <числовой тип данных> ::= NUMERIC[(<точность>[, <масштаб>])] | INTEGER | FLOAT[(<точность>)] | REAL
13. <временной тип данных> ::= DATE | TIME[(<точность>)]
14. <определение ограничений> ::= NOT NULL | UNIQUE | PRIMARY KEY
15. <название таблицы>, <название поля> ::= <идентификатор>
16. <идентификатор> ::= {<буква>|_}[{<буква>|_|<цифра>}...]
17. <длина>, <точность>, <масштаб> ::= <неотрицательное целое>
18. <неотрицательное целое> ::= <цифра>[<цифра>...]
19. <буква> := A|B|C|…|Z
20. <цифра> := 0|1|…|9