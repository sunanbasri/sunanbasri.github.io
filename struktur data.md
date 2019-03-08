stack (tumpukan)

lifo (last in first out)

stack() inisialisasi
push: penambahan data
pop: penghapusan data yng terdapat diposisi top
isEmpty: mengecek apakah stack sudah kosong
peek: informasi data yg terletak pada posisi top
size: informasi jumlah data yg tedapat pada stack

def stack():
    s=[]
    return(s)
def push(s,data):
    s.append(data)
def pop(s):
    data=s.pop()
    return(data)
def peek (s):
    return(s[len(s)-1])
def isEmpty(s):
    return (s==[])
def size (s):
    return (len(s))

contoh program membalikkan kata:

def balik (teks):
    a= stack()
    for i in range(len(teks)):
        push(a,teks[i])
    hasil=''
    for i in range (len(teks)):
        hasil=hasil+pop(a)
    return hasil
print(balik('arek'))

ekspresi aritmatik infix, prefix dan postfix
(A+B)xC ==> prefix= x+ABC post AB+Cx
(A+B)x(C+D)==> pre x+AB+CD post AB+CD+x
A+BxC ==> pre +AxBC post ABCx+
AxB-CxD ==> pre -xABxCD post ABxCDx-
Ax(B+C) post ABC+x
A+BxC post ABCx+