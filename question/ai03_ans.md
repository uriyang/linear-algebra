# 선형대수 문제 풀이 (기초 개념 정리)

---

## ✅ 문제 1: 행렬곱과 선형결합

### 문제

$$
A =
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix},
\quad
x =
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

---

### (1) y = Ax 계산

$$
Ax =
\begin{bmatrix}
1×2 + 2×1 \\
3×2 + 4×1
\end{bmatrix}
=
\begin{bmatrix}
4 \\
10
\end{bmatrix}
$$

---

### (2) 선형결합으로 표현

$$
A =
\begin{bmatrix}
| & | \\
c_1 & c_2 \\
| & |
\end{bmatrix}
=
\begin{bmatrix}
1 \\
3
\end{bmatrix},
\begin{bmatrix}
2 \\
4
\end{bmatrix}
$$

$$
Ax = 2c_1 + 1c_2
$$

$$
= 2
\begin{bmatrix}
1 \\
3
\end{bmatrix}
+
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
4 \\
10
\end{bmatrix}
$$

---

### ✔ 핵심

행렬곱은 열벡터의 선형결합이다.

---

## ✅ 문제 2: 연립방정식 (가우스 소거)

### 문제

$$
\begin{cases}
x + y + z = 6 \\
2x + y + z = 7 \\
x + 2y + z = 7
\end{cases}
$$

---

### 1. 확대행렬

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & 1 & 1 & 7 \\
1 & 2 & 1 & 7
\end{array}
\right]
$$

---

### 2. 첫 번째 열 소거

$$
R2 → R2 - 2R1
$$

$$
R3 → R3 - R1
$$

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -1 & -1 & -5 \\
0 & 1 & 0 & 1
\end{array}
\right]
$$

---

### 3. 두 번째 열 소거

$$
R2 → -R2
$$

$$
R3 → R3 - R2
$$

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & 1 & 5 \\
0 & 0 & -1 & -4
\end{array}
\right]
$$

---

### 4. 해 구하기

$$
z = 4
$$

$$
y + z = 5 → y = 1
$$

$$
x + y + z = 6 → x = 1
$$

---

### ✔ 최종 해

$$
x =
\begin{bmatrix}
1 \\
1 \\
4
\end{bmatrix}
$$

---

## ✅ 문제 3: 행렬식과 정칙행렬

### 문제

$$
A =
\begin{bmatrix}
1 & 2 \\
2 & 4
\end{bmatrix}
$$

---

### 1. 행렬식 계산

$$
det(A) = 1×4 - 2×2 = 4 - 4 = 0
$$

---

### 2. 해석

$$
(2,4) = 2×(1,2)
$$

→ 두 열이 선형종속

---

### 3. 결론

- det = 0  
- 역행렬 없음  
- 정칙행렬 아님  

---

### ✔ 핵심

det = 0 → 정보 손실 → 되돌릴 수 없음

---

## ✅ 문제 4: 좌표변환

### 문제

$$
v_1 = (1,1), \quad v_2 = (1,-1)
$$

$$
(2,3) = a v_1 + b v_2
$$

---

### 1. 식 세우기

$$
a(1,1) + b(1,-1) = (2,3)
$$

$$
(a+b, a-b) = (2,3)
$$

---

### 2. 연립

$$
a + b = 2
$$

$$
a - b = 3
$$

---

### 3. 풀이

$$
2a = 5 → a = 2.5
$$

$$
b = -0.5
$$

---

### ✔ 결과

$$
(2,3) = 2.5v_1 - 0.5v_2
$$

---

### ✔ 핵심

같은 벡터라도 기준(기저)에 따라 표현이 달라진다.

---

# 🔥 전체 핵심 요약

- Ax = 열벡터의 선형결합
- 가우스 소거 = 아래를 0으로 만드는 과정
- det = 0 → 정칙 아님
- 좌표변환 = 표현 바꾸기