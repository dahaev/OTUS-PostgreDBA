# HOMW WORK 1
## Работа с уровнями изоляции транзакции в PostgreSQL

В первый раз при селекте из второй сессии мы не видим запись (до коммита из первого терминала, но во время транзакции во втором). После коммита в первом терминале, мы уже увидим запись во втором терминале.

Это из за дефолтного уровня изоляции read commited. Мы видим транзакции подтвержденные другими транзакциями.


Во втором варианте тоже самое, за исключением, когда первая транзакция закоммичена, но мы еще находимся во время выполненитя второй, мы не видим новую запись в селекте, только после коммита, мы увидим запись закоммиченую первой транзакцией. Это уровень изоляции repeateble read. Все строки останутся неизменными до конца транзакции.

