## 날짜, 시간 계산하기

![](/Users/dychoi/Desktop/스크린샷 2018-08-09 오후 7.26.40.png)

​									[ user_dates ]



### DATE_ADD

- 기준 날짜에 입력된 값만큼 더하는 함수
- 음수를 더하는 것도 가능

```mysql
select
	user_id,
    registerd_date,
    DATE_ADD(registerd_date, INTERVAL 1 HOUR) as after_1_hour
from user_dates
```

###### ( register 는 registered의 오타.. )

![](/Users/dychoi/Desktop/스크린샷 2018-08-09 오후 7.30.40.png)



### DATE_SUB

* 기준 날짜에 입력된 값만큼 빼는 함수

```mysql
select
	user_id,
    registerd_date,
    DATE_SUB(registerd_date, INTERVAL -1 YEAR ) as befor_1_year
from user_dates
```

![](/Users/dychoi/Desktop/스크린샷 2018-08-09 오후 7.33.17.png)

