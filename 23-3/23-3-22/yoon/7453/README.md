7453

2<sup>28</sup>

내부 값은 int 범위 안.

각 배열당 4000개씩.

만약에 $4000^3$ 돌려서 넣어두고 마지막에 N으로 마무리한다고 하면

그리고 a,b,c,d는 idx이기 때문에 중복이 허용된다.

그렇게되면 unordered_map을 써야하나?

64 000 000 000

---

16 000 000

a,b 배열 더해서 나온 경우의 수 1600만

c,d 배열 더해서 나온 경우의 수 1600만

하나만 저장해두고 처리해도 괜찮잖아?

map으로 처리해서 같은 수가 나오면 ++만 처리해주자.

두개 섞을 땐 곱해주고.

더해주는건 int가 맞는데
경우의수 최대로 따지면 long long 나오나?

4000 * 4000 * 4000 * 4000
256000000000000

시간초과

---

unordered_map 사용할 때 string으로 사용하면 해쉬 처리에서 유리하다고 찾아와서 처리해봤지만 메모리 초과.

---

unordered_map이 아닌 vector<int>를 사용해야하는건가?

일단 long long은 나중에 처리하자. 이게 문제라면 시간초과가 아니라 틀렸습니다.가 뜰 것임.

a, b, c, d를 일반 벡터로 받고
값 두개 더한거를 map에 넣어보자.

4000 * 4000은 시간 얼마 안걸림.

---

틀렸습니다.

40%쯤에서 틀렸습니다인데, 사실 오히려 희소식인듯.
long long 처리 해주.

---

정답 맞추고 나서 hash map으로 한번 뚫어보자.

1차 시도. custom hash 추가.

하지만 unordered_map으론 여전히 시간초과.

https://codeforces.com/blog/entry/60737

gp_hash_table을 통해 처리해보자.

gp_hash_table 통해서 속도 향상 + custom_hash로 중복값 배제하니까 AC.