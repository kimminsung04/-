모의해킹 공부 기록

웹 해킹 기초

로그인 및 인증 관련 취약점

SQL Injection 로그인 우회

PortSwigger Web Security Academy에서 SQL Injection 실습

SELECT * FROM users WHERE username = 'administrator' AND password = 'test123';

password 또한 test123으로 동일해야하지만

로그인 아이디에 administrator'-- 를 집어넣게되면

아이디만 입력하는 칸에 SQL문법을 넣어 비밀번호가 맞는지 확인하는 절차를 무시하게 되었다.

SELECT * FROM users WHERE username = 'administrator'--' AND password = 'test123';

--'AND password = 'test123'; 을 주석처리하게되어 비밀번호가 맞는지 확인하는 절차를 무시하게 되었음.
