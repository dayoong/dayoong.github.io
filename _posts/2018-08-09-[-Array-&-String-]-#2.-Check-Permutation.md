### [ Problem ]

```
문자열 두 개가 주어졌을 때 서로 순열 관계에 있는지 확인하는 메서드 작성
```



### [ My solution ]

* 문자열은 알파벳 소문자로 가정

**1. 정렬 후 비교**

**2. 문자열에 포함된 문자의 출현 횟수가 같은지 검사**
* 알파벳 소문자 갯수+1의 배열을 2개 사용(0  인덱스는 사용 안함)

```python
str1 = "abbc"
str2 = "dacbbacabcbdefas"

check_arr1 = check_arr2 = [0] * 26

for i in range(26):
  if i < len(str1):
    index = ord(str1[i]) - 96
    check_arr1[index] += 1
    if i < len(str2):
      index = ord(str2[i]) - 96
      check_arr2[index] += 1
    else:
      break

flag = 0
for i in range(26):
  diff = check_arr1[i] - check_arr2[i]
  if diff != 0:
    flag = 1
    break

if flag == 1:
  print("순열 관계가 아닙니다")
else:
  print("순열 관계입니다")
```



### [ Another Solution ]

* **대소문자, 공백을 구분할 것인지 먼저 확인**
* **문자열 길이가 다르면 순열 관계일 수 없다**

**1. 정렬**
```
sort(String s)

permutation(String 1, String 2)
	if (1.len != 2.len):
		return false
	sort(1)
	sort(2)
	1과 2를 비교
```



**2. 문자열에 포함된 문자의 출현 횟수가 같은지 검사**
* ASCII 문자열인 경우
* [python 해법](https://github.com/careercup/CtCI-6th-Edition-Python/blob/e6bc732588601d0a98e5b1bc44d83644b910978d/Chapter1/2_Check%20Permutation/CheckPermutation.py)



[ 출처 ] 코딩 인터뷰 완벽 분석