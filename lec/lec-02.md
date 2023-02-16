# Лекция 02

Программа на языке Лисп является символьным выражением, вычисляемым
интерпретатором.

Функции:

- базисные;
- функции ядра;
- пользовательские.

Чистая функция не имеет побочных эффектов, а её значение зависит только от её
аргументов.

Особая форма может иметь переменное число аргументов, а также вычислять их в
особом порядке.

Базисные функции:

- `atom`:

``` lisp
* (atom nil)
t
* (atom (cons nil nil))
nil
```

- `car`:

``` lisp
* (car (cons nil t))
nil
```

- `cdr`:

``` lisp
* (cdr (cons nil t))
t
```

- `cons`:

``` lisp
* (cons nil nil)
(nil)
* (cons nil t)
(nil . t)
* (cons t nil)
(t)
* (cons t t)
(t . t)
```

- `eq`:

``` lisp
* (eq nil nil)
t
* (eq nil t)
nil
* (eq t nil)
nil
* (eq t t)
t
```

Базисные особые формы:

- `cond`:

``` lisp
* (defun collatz (x) (cond ((evenp x) (/ x 2)) ((oddp x) (+ (* 3 x) 1))))
* (collatz 1)
4
* (collatz 2)
1
```
