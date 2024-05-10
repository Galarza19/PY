#Dependencias
def may(a ,b):
    m = a
    if(b > a):
        m = b
    return b

def men(a ,b):
    m = a
    if(b < a):
        m = b
    return b

def pos(n):
    return n > 0

def neg(n):
    return n < 0

def par(n):
    return n % 2 == 0

def impar(n):
    return n % 2 != 0

def primo(n):
    c=0
    i=1
    while(i <= n):
        if(n % i == 0):
            c += 1
        i += 1
    return c == 2

#Digitos
#1
def sumdig(n):
    s = 0
    while(n > 0):
        s = s + (n % 10)
        n = n // 10
    return s

#2 
def cantdig(n):
    c = 0
    while(n > 0):
        c += 1
        n = n // 10
    return c

#3 
def maydig(n):
    m = 0
    while(n > 0):
        if(n % 10 > m):
            m = n % 10
        n = n // 10
    return m

#4
def puropar(n):
    while(n > 0):
        if(impar(n % 10)):
            return False
        n = n // 10
    return True

#5
def sumprimo(n):
    s = 0
    while(n > 0):
        if(primo(n % 10)):
            s = s + (n % 10)
        n = n // 10
    return s


#Divisores
# divisor par
def divisores_1(n):
    i = 1
    while i <= n:
        if n % i == 0 and par(i):
            print(i)
        i = i + 1
# divisor primo
def divisores_2(n):
    i = 1
    while i <= n:
        if n % i == 0 and primo(i):
            print(i)
        i = i + 1
# cantidad de divisores 
def divisores_3(n):
    i = 1
    cont = 0
    while i <= n:
        if n % i == 0:
            cont = cont + 1
        i = i + 1
    print(cont)    
# divisores de mayor a menor 
def divisores_4(n):
    i = n
    while i > 0:
        if n % i == 0:
            print (i)
        i = i - 1
# divisores de menor a mayor 
def divisores_5(n):
    i = 1
    while i <= n:
        if n % i == 0:
            print (i)
        i = i + 1    
# divisores de n desde a hasta b
def divisores_6(n,a,b):
    i = a
    while i <= b:
        if n % i == 0:
            print(i)
        i = i + 1

#Ciclos
#tabla de par por impar 
def ciclos_1(n):
    i = 1
    while i <= n:
        j = 1
        while j <= n:
            if par(i) and impar(j):
                print(i, "x",j,"=",i*j)
            j = j + 1
        i = i + 1
# tabla de pares 
def ciclos_2(n):
    i = 1
    while i <= n:
        j = 1
        while j <= n:
            if par(i) and par(j):
                print(i, "x",j,"=",i*j)
            j = j + 1
        i = i + 1
# tabla de primer argumento primo
def ciclos_3(n):
    i = 1
    while i <= n:
        j = 1
        while j <= n:
            if primo(i):
                print(i, "x",j,"=",i*j)
            j = j + 1
        i = i + 1
# tabla primo por negativo
def ciclos_4(n):
    i = 1
    while i <= n:
        j = -1
        while j <= n:
            if primo(i) and neg(j):
                print(i, "x",j,"=",i*j)
            j = j - 1
        i = i + 1
# tabla de primo por primo
def ciclos_5(n):
    i = 1
    while i <= n:
        j = 1
        while j <= n:
            if primo(i) and primo(j):
                print(i, "x",j,"=",i*j)
            j = j + 1
        i = i + 1    


#llamdas
def main():
    print(sumdig(123))
    print(cantdig(123))
    print(maydig(129))
    print(puropar(824))
    print(sumprimo(975))

if __name__ == "__main__":
    main()