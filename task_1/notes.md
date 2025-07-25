### Условие задачи 
Чем дольше Иван слышал этот звук, тем больше сходил с ума! В отчаянии он решил отложить все свои дела, чтобы наконец 
вычислить, кто из окружающих его коллег исподтишка выполняет это действие.

Для этого Иван подошёл к каждому из коллег и попросил высказать своё мнение о сложившейся ситуации. Ответы коллег он 
записал в одном из следующих форматов:
- `A: I am x!` → A +2
- `A: I am not x!` → A -1
- `A: B is x!` → B +1
- `A: B is not x!` → B -1

### Входные данные 

Первая строка входных данных содержит натуральное число 
t (1 ≤ t ≤ 10^5) — количество наборов входных данных. Следующие строки содержат подряд идущие наборы входных данных.
Рассмотрим очередной такой набор.
Первая строка набора входных данных содержит натуральное число n
(1 ≤ n ≤ 10^5) — количество высказываний. Далее идёт n строк в формате, описанном в условии задачи, где A и B обозначают
имена подозреваемых, а x — какое-то действие.
Гарантируется, что:
- A, B и x состоят только из букв английского алфавита и не длиннее 10 символов. При этом x
 содержит только строчные буквы. A и B же начинаются с заглавной буквы, а все остальные буквы строчные.
- В рамках одного набора входных данных действие (x) не меняется между высказываниями.
- Сумма n по всем наборам входных данных не превышает 10^5

### Выходные данные
Для каждого набора входных данных выведите имя того, кто по описанному алгоритму набрал наибольшее количество очков,
в формате "A is x.", где A - это имя подозреваемого, а х - действие. Если наибольшее количество очков набрали несколько 
подозреваемых, выведите их всех в описанном формате в лексикографическом порядке, разделяя предложения переносами строк.

### План решения 

1. Прочитать `t` — количество наборов.
2. Для каждого набора:
   - Прочитать `n` — число высказываний.
   - Для каждого высказывания:
     - Распознать тип фразы (I am / I am not / B is / B is not).
     - Извлечь имена и начислить очки нужному человеку.
3. После всех фраз — найти **максимальное** значение очков.
4. Выбрать **всех людей с этим значением**.
5. Отсортировать по алфавиту.
6. Вывести в формате `Name is x.`
