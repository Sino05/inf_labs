# Отчет по лабораторной работе № 5

## по курсу "Фундаментальная информатика"

Студент группы М8О-108Б-23 Сино Шералиев Дилшодович

Работа выполнена

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Машина Тьюринга
2. **Цель работы**: Составить программу машины Тьюринга в четвёрках, выполняющую заданное действие над словами, записанными на ленте.
3. **Задание**: Вычисление поразрядной дизъюнкции двух двоичных чисел.
4. **Идея, метод, алгоритм решения задачи**: 
- Установить эммулятор машины Тьюринга
- Опробовать "команды"
- Выполнить задание
5. **Сценарий выполнения работы**: 

| Входные данные | Выходные данные |
|----------------|-----------------|
| 10 11          | 11              |
| 101 10         | 111             |
| 0 1            | 1               |
| 00 101         | 101             |

6. **Протокол**:
```
00, ,<,RER
RER,1,*,TRUE
RER,0,$,FALSE
RER,*,<,RER
RER,$,<,RER
RER, ,<,proverka

TRUE,0,<,TRUE
TRUE,1,<,TRUE
TRUE,*,<,TRUE
TRUE, ,<,TRUE2

TRUE2,1,&,nazad
TRUE2,0,^,nazad
TRUE2,&,<,TRUE2
TRUE2,^,<,TRUE2
TRUE2, ,>,nazad

nazad,&,>,nazad
nazad,^,>,nazad
nazad, ,>,nazad2

nazad2,1,>,nazad2
nazad2,0,>,nazad2
nazad2,*,>,nazad2
nazad2,$,>,nazad2
nazad2, ,>,nazad3

nazad3, ,1,NAZAD
nazad3,1,>,nazad3
nazad3,0,>,nazad3

NAZAD,1,<,NAZAD
NAZAD,0,<,NAZAD
NAZAD, ,<,RER

FALSE,0,<,FALSE
FALSE,1,<,FALSE
FALSE,$,<,FALSE
FALSE, ,<,FALSE2

FALSE2,1,&,nazadtr
FALSE2,0,^,nazadfl
FALSE2,&,<,FALSE2
FALSE2,^,<,FALSE2
FALSE2, ,>,nazadfl

nazadfl,^,>,nazadfl
nazadfl,&,>,nazadfl
nazadfl, ,>,nazadfl2

nazadfl2,1,>,nazadfl2
nazadfl2,0,>,nazadfl2
nazadfl2,$,>,nazadfl2
nazadfl2,*,>,nazadfl2
nazadfl2, ,>,nazadfl3

nazadfl3,1,>,nazadfl3
nazadfl3,0,>,nazadfl3
nazadfl3, ,0,NAZAD

nazadtr,^,>,nazadtr
nazadtr,&,>,nazadtr
nazadtr, ,>,nazadtr2

nazadtr2,1,>,nazadtr2
nazadtr2,0,>,nazadtr2
nazadtr2,$,>,nazadtr2
nazadtr2,*,>,nazadtr2
nazadtr2, ,>,nazadtr3

nazadtr3,1,>,nazadtr3
nazadtr3,0,>,nazadtr3
nazadtr3, ,1,NAZAD

proverka,&,<,proverka
proverka,^,<,proverka
proverka,1,&,nazadtr
proverka,0,^,nazadfl
proverka, ,>,zamena

zamena,&,1,zamena
zamena,1,>,zamena
zamena,^,0,zamena
zamena,0,>,zamena
zamena, ,>,zamena1

zamena1,*,1,zamena1
zamena1,1,>,zamena1
zamena1,$,0,zamena1
zamena1,0,>,zamena1
zamena1, ,*,end

end,*,>,WOW

WOW,1,>,WOW
WOW,0,>,WOW
WOW, ,<,pr

pr,1,%,tr
pr,%,<,pr
pr,@,<,pr
pr,0,@,fl
pr,*,>,del

tr,%,>,tr
tr,@,>,tr
tr, ,>,tr2

tr2, ,1,naz
tr2,1,>,tr2
tr2,0,>,tr2

fl,@,>,fl
fl,%,>,fl
fl, ,>,fl2

fl2, ,0,naz
fl2,1,>,fl2
fl2,0,>,fl2

naz,1,<,naz
naz,0,<,naz
naz, ,<,pr

del,%, ,del
del,@, ,del
del, ,>,del
del,1,=,sdv
del,0,=,sdv

sdv,1, ,sdv1
sdv,0, ,sdv0
sdv, ,<,fargot

sdv1, ,<,sdv11
sdv11, ,1,sdv11
sdv11,1,>,del2
sdv11,*,>,predans

predans, ,1,predans
predans,1,<,predans
predans,*, ,ans

sdv0, ,<,sdv00
sdv00, ,0,sdv00
sdv00,0,>,del2
sdv00,*,>,predans2

predans2, ,0,predans2
predans2,0,<,predans2
predans2,*, ,ans

del2, ,>,sdv

fargot, ,<,fargot
fargot,1,<,fargot
fargot,0,<,fargot
fargot,*,>,del

ans, ,>,ANS

ANS,1,>,ANS
ANS,0,>,ANS
ANS, , ,ANS
```
7. **Замечания автора**: было сложно понять.
8. **Выводы**: Я научился програмировать на машине тьюринга.