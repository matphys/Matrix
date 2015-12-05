class Matrix:

    A = None
    m = None
    n = None

    def __init__(self, m, n=None):
        if m <= 0 or n <= 0 or type(m) != int or type(n) != int:
            raise Exception(ValueError)
        self.A = [[0]*n for i in range(m)]
        self.m = m
        self.n = n

    def __add__(self, other):
        if self.m == other.m and self.n == other.n:
            for j in range(self.m):
                for i in range(self.n):
                    self.A[j][i] += other.A[j][i]
            return self
        else:
            print('Разные размеры матриц!')


    def determinant(self):
        if self.m == self.n:
            if self.n == 1:
                return self.A[1][1]
            elif self.n == 2:
                return self.A[1][1]*self.A[2][2] - self.A[1][2]*self.A[2][1]
            elif self.n == 3:
                return self.A[1][1]*self.A[2][2]*self.A[3][3] + self.A[1][2]*self.A[2][3]*self.A[3][1] + self.A[1][3]*self.A[2][1]*self.A[3][2] - self.A[1][3]*self.A[2][2]*self.A[3][1] - self.A[1][2]*self.A[2][1]*self.A[3][3] - self.A[1][1]*self.A[2][3]*self.A[3][2]
            else:
                print('Слишком большая матрица!')
        else:
            print('Матрица не квадратная!')


    def __eq__(self, other):
        bull = True
        if self.n == other.n and self.m == other.m:
            for j in range(self.m):
                for i in range(self.n):
                    if self.A[j][i] != other.A[j][i]:
                        bull = False
        else:
            bull = False
        return bull


    def get(self, i, j):
        if i <= self.m and j <= self.n:
            raise Exception(ValueError)
        else:
            return self.A[i][j]


    def get_m(self):
        return self.m


    def get_n(self):
        return self.n


    def get_size(self):
        return self.m, self.n
        
    def set(self,i,j,value):
        self.A[i][j]=value
        
    def __sub__(self, other):
        P=self.A
        B=self.A
        U=other.A
        if self.m==other.m and self.n==other.n:
            for x in range(self.m):
                for y in range(self.n):
                    P[x][y]=B[x][y]-U[x][y]
        self.P=P
        return self.P
