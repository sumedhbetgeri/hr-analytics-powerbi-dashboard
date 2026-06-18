# DAX Measures

## Employee Count

```DAX
Employee Count =
COUNT(Employee[EmployeeNumber])
```

Counts the total number of employees.

---

## Attrition Count

```DAX
Attrition Count =
CALCULATE(
    [Employee Count],
    Employee[Attrition] = "Yes"
)
```

Counts employees who have left the organization.

---

## Attrition Rate

```DAX
Attrition Rate =
DIVIDE([Attrition Count], [Employee Count], 0)
```

Calculates the percentage of employees who left.

---

## Active Employees

```DAX
Active Employees =
[Employee Count] - [Attrition Count]
```

Calculates employees currently working.

---

## Average Age

```DAX
Average Age =
AVERAGE(Employee[Age])
```

Returns the average age of employees.
