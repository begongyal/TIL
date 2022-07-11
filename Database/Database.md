Foreign Key 삭제

```
ALTER TABLE 테이블명 DROP FOREIGN KEY 포린키이름;

ALTER TABLE feed DROP FOREIGN KEY feed_ibfk_3;
```

-------------------

Foreign Key 추가(여기서 포린키 이름은 안적으면 기본 이름으로 적용됨)

```
ALTER TABLE 테이블명 ADD CONSTRAINT 포린키이름 FOREIGN KEY 자식속성 REFERENCES 부모테이블명(자식속성이 참고할 부모속성) ON DELETE CASCADE;

ALTER TABLE feed ADD CONSTRAINT FOREIGN KEY (user_id) REFERENCES user(id) ON DELETE CASCADE;
```

--------------------

데이터베이스 카피하는법

https://www.mysqltutorial.org/mysql-copy-database/

-----------------------------

오토커밋 꺼놓았을때 일어나는 일들

https://dev.mysql.com/doc/refman/5.6/en/innodb-autocommit-commit-rollback.html

"If autocommit mode is disabled within a session with SET autocommit = 0, the session always has a transaction open.
A COMMIT or ROLLBACK statement ends the current transaction and a new one starts."

"A session that has autocommit enabled can perform a multiple-statement transaction by starting it with
an explicit START TRANSACTION or BEGIN statement and ending it with a COMMIT or ROLLBACK statement. See Section 13.3.1, “START TRANSACTION, COMMIT, and ROLLBACK Statements”."

---------------------------

Read uncommitted, Read committed, Repeatable read, serializable에 대해서 추후에 추가 
