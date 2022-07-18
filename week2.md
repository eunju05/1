## <연습문제 2-1 재귀적 arrayMax>
```
Alg arrayMax(A, n)
  intput array A of n integers
  output maximum element of A
  
1. if (n = 1)
    return A[0]
2. else
    return max(A[n-1], arrayMax(A, n-1))
```

## <연습문제 2-2 재귀적 arrayMaxMin>
```
Alg arrayMaxMin(A, n)
  input array A of n integers
  output maximum element and minimum element of A
 
1. if (n = 1)
    return A[0], A[0]
2. else
    l,s ← arrayMaxMin(A, n-1)
    l ← max(A[n-1], l)
    s ← min(A[n-1], s)
    return l,s
```
>잘 모르겠어서 답지 참고

## <연습문제 3-1 배열의 크기>
3차원 배열 A[-3..2, 1..4, 0..9]

>(2-(-3)+1)(4-1+1)(9-0+1) = 6x4x10 = 240

2차원 배열 A[1..M, -1..N]

>(M-1+1)(N-(-1)+1) = M(N+2)

## <연습문제 3-2 배열원소의 저장 순서>
2차원 배열 A[-1..3, 0..5]의 원소 A[2, 3]의 위치

>행우선 순서 : [(k1-LB1)(UB2-LB2+1)]+(k2-LB2) = 21
>
>열우선 순서 : [(k2-LB2)(UB1-LB1+1)]+(k1-LB1) = 18

## <연습문제 3-3 배열원소의 저장 순서>
행우선 3차원 배열 A[0..2, -1..M, 0..N]의 원소 A[i, j, k]의 위치
>[(k1-LB1)(UB2-LB2+1)(UB3-LB3+1)]+(k2-LB2)(UB3-LB3+1)+(k3-LB3) = i(M+2)(N+1)+(j+1)(N+1)+k
