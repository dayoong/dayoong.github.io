#### [ Problem ]

```
문자열이 주어졌을 때, 문자열에 같은 문자가 중복되어 등장하는지 확인하는 알고리즘
```



#### [ My solution ]

**1. 알파벳 크기의 배열을 사용**

```
alphabet_arr = [0] * 27
flag = 0
for 문자열 길이:
	index = 문자열[i] - 64
	if alphabet_arr[index] == 1:
		중복 있음
		flag = 1
	alphabet_arr[index] = 1
if flag == 0:
	중복 없음
```



#### [ 해법 ]

**1. i번째 문자가 배열 내에 존재하는지 표시하는 boolean 배열을 사용**

* ASCII 문자열일 경우
* 문자열의 길이가 ASCII 문자 집합 크기 보다 클 경우 `return false`
* 같은 원소에 두 번 접근하면 `return false`

```python
if (문자열_len > 128) return false
char_set = [] * 128
for i in range(len(문자열_len)):
	if (char_set[i]):
        return false
    char_set[i] = true
return true
```

* 시간 복잡도 O(n) / 공간 복잡도 O(1)



**2. 문자열을 정렬한 뒤 문자열을 처음부터 훑어 가면서 검사**

* 정렬 알고리즘이 공간을 추가 사용



[ 출처 ] 코딩 인터뷰 완벽 분석