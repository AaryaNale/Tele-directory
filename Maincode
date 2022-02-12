import pickle
def enter():
    n=int(input('Enter total number of enteries: '))
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','wb')
    for i in range(0,n):
        a=input('Enter user name: ')
        b=int(input('Enter phone number: '))
        c=input('Enter address: ')
        rec={'User':a,'Phone number':b,'Address':c}
        pickle.dump(rec,f)
    f.close()
def show():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','rb')
    while True:
        try:
            rec=pickle.load(f)
            print(rec)
        except EOFError:break
    f.close()
def search1():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','rb')
    tmp=int(input('Enter phone number to be searched: '))
    while True:
        try:
            rec=pickle.load(f)
            if (rec['Phone number']==tmp):
                print('User:',rec['User'])
                print('Phone number:',rec['Phone number'])
                print('Address: ',rec['Address'])
        except EOFError:break
    f.close()
def search2():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','rb')
    tmp3=input('Enter the name: ')
    while True:
        try:
            rec=pickle.load(f)
            if (rec['User']==tmp3):
                print('User:',rec['User'])
                print('Phone number:',rec['Phone number'])
                print('Address: ',rec['Address'])
        except EOFError:break
    f.close() 
def modify():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','rb')
    L=[]
    while True:
        try:
            rec=pickle.load(f)
            L.append(rec)
        except EOFError:break
    f.close()
    tmp1=input('Enter name whose number is to be modified: ')
    for rec in L:
        if rec['User']==tmp1:
            tmp0=int(input('Enter the new phone number: '))
            rec['Phone number']=tmp0
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','wb')
    for x in L:
        pickle.dump(x,f)
    f.close()
def append():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','ab')
    r1=input('Enter the new username: ')
    r2=int(input('Enter the new phone number: '))
    r3=input('Enter your present Address: ')
    rec1={'User':r1,'Phone Number':r2,'Address':r3}
    pickle.dump(rec1,f)
    f.close()
def delete():
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','rb')
    l=[]
    while True:
        try:
            rec=pickle.load(f)
            l.append(rec)
        except EOFError:break
    f.close()
    f=open('C:\\Users\Ganesh\Desktop\Telephone directory.bin','wb')
    tmp2=input('Whose record is to be deleted? Please enter the registered Username: ')
    for t in l:
        if (t['User']==tmp2):
            continue
        pickle.dump(t,f)
    f.close()
print('1: To search the User according to the Phone number')
print('2: To search the Phone number according to the User')
print('3: To modify an existing record')
print('4: To add a new Record')
print('5: To delete an  existing record')
print('6: To display the entire directory')
enter()
q=int(input('Enter number of choices: '))
for y in range(0,q):
    r=int(input('Enter choice: '))
    if r==1:
        search1()
    if r==2:
        search2()
    if r==3:
        modify()
    if r==4:
        append()
    if r==5:
        delete()
    if r==6:
        show()


                 
               
    
        
        
