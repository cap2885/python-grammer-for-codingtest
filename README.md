## python-grammer-for-codingtest

## 수 자료형
(1) 정수형  
코딩테스트에서는 대부분의 경우 정수형을 다루는 문제가 출제됨.

(2) 실수형    
**지수표현방식
1e9는 10의 9제곱과 같다.  
예를 들어, 최단 경로로 가능한 최댓값이 10억 미만이라면 무한(INF)을 1e9로 표현할 수 있다.  

1e4 # 10000  
75.25e1 # 752.5  
3954e-3 # 3.954  

(3) 2진수  
a = 0.3 + 0.6  
print(a)  
\# 0.89999999999 

(4) round 함수  
첫 번째 인자 - 실수형 데이터  
두 번쨰 인자 - (반올림하고자 하는 위치 - 1)  

ex) 123.456을 소수점 셋째 자리에서 반올림하려면, round(123.456, 2)  
결과 # 123.46  

(5) 나누기 연산자(/)  
a = 7  
b = 3  
print(a / b) # 2.33333333333335  
print(a % b) # 1  
print(a // b) # 2  

(6) 거듭제곱 연산자(**)  

a = 5  
b = 3  
print(a**b) # 125  

## 리스트 자료형  

(1) 리스트 초기화
\# 크기가 N이고, 모든 값이 0인 1차원 리스트 초기화  
n = 5  
a = [0] * n  
print(a) # [0, 0, 0, 0, 0]  

(2) 리스트의 인덱싱과 슬라이싱  
\# 뒤에서 세 번째 원소 출력  
print(a[-3])  

\# 네 번째 원소 값 변경  
a[3] = 7

\# 두 번째 원소~ 네 번째 원소까지  
print(a[1 : 4])  

(3) 리스트 컴프리핸션  
\# 0부터 19까지의 수 중에서 홀수만 포함하는 리스트  
array = [i for i in range(20) if i % 2 == 1]  
print(array) # [1, 3, 5, 7, ''', 19]  

\# N X M 크기의 2차원 리스트 초기화 (반드시 리스트 컴프리핸션 사용해야함!)   
n = 3  
m = 4
array = [[0] * m for _ in range(n)]  
print(array) # [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]  

(4) 리스트 관련 기타 메서드  
리스트.append(값) - 리스트에 원소 하나 삽입  
리스트.sort() - 오름차순 정렬  
리스트.sort(reverse = True) - 내림차순 정렬  
리스트.reverse() - 리스트의 원소의 순서를 모두 뒤집음  
리스트.insert(삽입할 위치 인덱스, 삽입할 값) - 특정한 위치에 원소를 삽입  
리스트.count(특정 값) - 특정한 값을 가지는 데이터의 개수를 셀 때 사용  
리스트.remove(특정 값) - 특정한 값을 갖는 원소를 제거하는데, 값을 가진 원소가 여러 개면 하나만 제거한다.  

a = [1, 2, 3, 4]  
a.insert(1,3)  
print(a) # [1, 3, 2, 3, 4]  

a.remove(3)  
print(a) # [1, 2, 3, 4]  

(5) remove_set 이용  
insert()와 remove() 함수의 시간 복잡도는 O(N)이므로, '시간 초과'가 나올 수 있음. -> remove_set 이용  

a = [1, 2, 3, 4, 5, 5, 5]  
remove_set = {3, 5}  

result = [i for i in a if i not in remove_set]  
print(result) # [1, 2, 4]  

## 문자열 자료형  

(1) 백슬래시 \  
백슬래시(\)를 이용하여 큰따옴표나 작은따옴표를 문자열에 포함시킬 수 있음.  

## 튜플 자료형  

- 튜플은 한 번 선언된 값을 변경할 수 없다.
- 튜플은 () 소괄호를 이용한다.
- 튜플은 원소의 대입이 불가능하다.

튜플 자료형은 그래프 알고리즘을 구현할 때 자주 사용함. 다익스트라 최단 경로 알고리즘처럼 최단 경로를 찾아주는 알고리즘의 내부에서는 우선순위 큐를 이용함. 우선순위 큐에 한 번들어간 값은 변경되지 않음.  

## 사전 자료형  

- 키(key)와 값(value)의 쌍을 데이터로 가지는 자료형.
- 데이터의 겁색 및 수정에 있어서 O(1)의 시간복잡도.

키(key)      값(value)  
사과         Apple  
바나나       Banana  

(1) 사전 자료형 관련 함수  

data = dict()  
data['사과'] = 'Apple'  
data['바나나'] = 'Banana'  

\# 키 데이터만 담은 리스트  
key_list = data.keys()  

\# 값 데이터만 담은 리스트  
value_list = data.values()

\# 각 키에 따른 값을 하나씩 출력  
for key in key_list :
    print(data[key])

참고자료) 이것이 코딩테스트다, 나동빈



