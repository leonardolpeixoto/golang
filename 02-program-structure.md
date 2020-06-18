# Program Structure

## Names

The names of Go functions, variables, constants, types, statement labels, and packages must begins with a letter or an underscore and may have any number of additional letters, digits, and underscores. The names are **case sensitive**.

Go has [25 keywords](https://golang.org/ref/spec#Keywords), they can't be  used as names.

If an entity is declared within a functions, it is local to that function. If declared outside of a function, however, it is visible in all files of the package to which it belongs. The case of the first latter of a name determines its visibility across packages boundaries. If the name begins with an upper-case letter, it is exported, which means that it is visible and accessible outside of its own package and my be referred to by other parts of the program. Package names themselves are always in lower case.

## Variables

A **var** declaration creates a variable of a particular type, attaches a name to it, and sets its initial value.

```golang
var name type = expression
```

Either the type or the = *expression* part may be omitted, but not both. If the type is omitted, it is determined by the initializer expression. If the expression is omitted, the initial value is the [zero value](https://golang.org/ref/spec#The_zero_value) for the type.

A set of variables can also be initialized bt calling a function that returns multiple values:

```golang
var file, err = os.Open(name)
```

