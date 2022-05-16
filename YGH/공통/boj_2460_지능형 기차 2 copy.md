# 문제 제목
[:link: 지능형 기차 2](https://www.acmicpc.net/problem/2460)  
<br>

### 풀이 방식
```python
STATION_COUNT = 10

people_count = 0 # 기차에 탄 인원
max = 0 # 최대 사람 수 
for i in range(STATION_COUNT):
    get_off_num, get_on_num = map(int, input().split())

    # 탄 사람 수에 내린 사람 수를 뺀 값을 기차에 탄 인원에 더한다.
    people_count += get_on_num - get_off_num

    max = people_count if people_count > max else max
    
print(max)

```