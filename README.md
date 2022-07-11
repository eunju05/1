## <연습문제 1-1 합>
```
Alg sum(n)

1. sum ← 0		{1}
2. for i ← 0 to n	{n}
	sum ← sum + i	{n}
3. return sum		{1}
			{Total O(n) //O(1 + n + n + 1) = O(2n + 2) = O(n)}
```

## <연습문제 1-2 한 라인에 한 숫자 인쇄>
```
Alg printDigits(n)

1. while (n > 0)	{log(n) + 1}
	d ← n % 10	{log(n) + 1}
	write(d)	{log(n) + 1}
	n ← n / 10	{log(n) + 1}
2. return 		{1}
			{Total O(log(n)) //O(4log(n) + 5) = O(log(n))}
```

## <연습문제 1-3 나머지 연산>
```
Alg modulo(a,b)

1. while(a >= b)	{a/b}
	a ← a - b	{a/b}
2. return a		{1}
			{Total O(a/b)}
```

## <연습문제 1-3 Big-Oh 구하기>
```
Alg a1(m)

1. p ← 1		{1}
2. for i ← i to 3m	{3m}
	p ← p*i		{3m}
			{Total O(m)}
```
```
Alg a2(t)

1. p ← 1		{1}
2. for i ← i to t^2	{t^2}
	p ← p*i		{t^2}
			{Total O(T^2)}
```
```
Alg a3(p)

1. s ← 0		{O(1)}
2. for n ← 1 to 2p	{O(p)}
	for j ← 1 to n		{O(p^2)}
		s ← s + n	
			{Total O(p^2)}
```
```
Alg a4(n)

1. s ← 0		{O(1)}
2. for i ← 1 to n	{O(n)}
	for j ← 1 to i^2		{O(n^3)}
		s ← s + i	
			{Total O(n^3)}
```
```
Alg a5(n)

1. s ← 0		{O(1)}
2. for k ← 1 to n^2	{O(n^2)}
	for j ← 1 to k		{O(n^3)}
		s ← s + k	
			{Total O(n^3)}
```
```
Alg a6(k,n)

1. s ← 0		{O(1)}
2. for i ← 1 to n^2	{O(n^2)}
	for j ← 2 to k		{O(k*n^2)}
		s ← s + k	
			{Total O(k*n^2)}
```

## <연습문제 1-5 Big-Oh 증명>
> A. "(n + 1)^5 = O(n^5)"임을 보여라.
>> n ≥ n0 에 대해 (n + 1)^5 ≤ c(n^5)이 성립하는 c > 0 및 n0 ≥ 1이 필요하다. c=33이고 n0=1일 때 성립하므로 (n + 1)^5 = O(n^5)이다.

> B. "2^(n+1) = O(2^n)"임을 보여라.
>> n ≥ n0 에 대해 2^(n+1) ≤ c(2^n)이 성립하는 c > 0 및 n0 ≥ 1이 필요하다. c=3이고 n0=1일 때 성립하므로 2^(n+1) = O(2^n)이다.
