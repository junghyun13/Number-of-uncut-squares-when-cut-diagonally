# Number-of-uncut-squares-when-cut-diagonally
# Find the number of uncut squares by cutting one diagonal of a square with a given width and length. 가로와 세로가 주어진 정사각형의 대각선을 1번 잘라서 잘리지 않은 가로,세로 1인 정사각형의 개수를 구하기
def square(a,b):
    a,b=max(a,b),min(a,b)
    while(True):
        r=a%b 
        if r==0:
            return b
        else:
            a=b
            b=r #r이 0이 아닌 숫자이면 a,b에 각각 b,r을 넣어서 r이 0이 될때까지 반복하면 b가 최대공약수가 됨     
def solution(w,h):
    area=w*h
    gcf=square(w,h)
    return area-((w+h)-gcf) #gcf는 최대 공약수 대각선을 그어서 사용할수 없는 사각형을 구하는법은 넓이-(가로+세로-최대공약수)
a=solution(8,12)
print(a)
# result--> 80
