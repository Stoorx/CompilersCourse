**Упражнение 2.2.4.** Постройте однозначные контекстно-свободные грамматики
для каждого из следующих языков. В каждом случае покажите корректность вашей грамматики.

```
а) Арифметические выражения в постфиксной записи.
б) Левоассоциативный список идентификаторов, разделенных запятыми.
в) Правоассоциативный список идентификаторов, разделенных запятыми.
г) Арифметические выражения, состоящие из целых чисел и идентификаторов с четырьмя бинарными операторами +, -, *, /.
! д) Добавьте унарные “плюс” и “минус” к арифметическим операторам из г.
```

---

*Задание А*

```EBNF
Expr → Expr Expr Op | Digit
Op → + | - | * | /
Digit → 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
```

*Задание Б*

```EBNF
List → List , Element | Element
```

*Задание В*

```EBNF
List → Element , List | Element
```

*Задание Г*

```EBNF
SumExpr → SumExpr SumOp MulExpr | MulExpr 
MulExpr → MulExpr MulOp Number | Number
SumOp → + | -
MulOp → * | /
```

*Задание Д*

```EBNF
SumExpr → SumExpr SumOp MulExpr | MulExpr 
MulExpr → MulExpr MulOp UnaryExpr | UnaryExpr
UnaryExpr → SumOp Number | Number
SumOp → + | -
MulOp → * | /
```
