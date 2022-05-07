# Multibrand_retail
import pandas as pd
import pymysql
myConnection = pymysql.connect( host='localhost',
                                user='root',
                                password='Sivababu@1997',
                                db='retail')
cur=myConnection.cursor()
cur.execute('select * from ethnic_wear ')
myresult=cur.fetchall()


def kk(cat_code):
    cur.execute('select cat_code from kk')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select * from kk where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        print(myresult)
    else:
        print('sorry product is not available rightnow!')
        
def p(cat_code):
    cur.execute('select cat_code from kk')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select final_price from kk where cat_code=%s')
    
        user=cat_code
        cur.execute(syn,user)
        myresult=(cur.fetchall())
        myresult=list(map(lambda x:x[0],myresult))
        print(myresult)
        syn1=('select description from kk where cat_code=%s')
        user=cat_code
        cur.execute(syn1,user)
        myresult1=cur.fetchall()
        myresult1=list(map(lambda x:x[0],myresult1))
        print(myresult1)
        print('yes or no')
        ch=input('Enter:')
        if ch=='yes':
            a.append(myresult)
            b.append(myresult1)
            print(a)
            print(b)
            i=list(map(lambda x : x[0],a))
            j=list(map(lambda x : x[0],b))
            dicts=dict(zip(i,j))
            print(dicts)
            print('Item is added to cart')
            
        elif ch=='no':
            print('Do you like to complete the order?')
            ch=input('enter:')
            for letter in ch:
                if letter =='yes':
                    break

            print('Thankyou for your visit sir!')
                
           

    else:
        print('sorry product is not available rightnow!')       

def p1(cat_code):
    cur.execute('select cat_code from es')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select final_price from es where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        myresult=list(map(lambda x:x[0],myresult))
        print(myresult)
        syn1=('select description from es where cat_code=%s')
        user=cat_code
        cur.execute(syn1,user)
        myresult1=cur.fetchall()
        myresult1=list(map(lambda x:x[0],myresult1))
        print(myresult1)
        print('yes or no')
        ch=input('Enter:')
        if ch=='yes':
            a.append(myresult)
            b.append(myresult1)
            print(a)
            print(b)
            i=list(map(lambda x: x[0],a))
            j=list(map(lambda x: x[0],b))
            dicts=dict(zip(i,j))
            print(dicts)
            print('Item is added to cart')
            
        elif ch=='no':
            print('Do you like to complete the order?')
            ch=input('enter:')
            for letter in ch:
                if letter =='yes':
                    break

            print('Thankyou for your visit sir!')
            
    else:
        print('sorry product is not available rightnow!')

def es(cat_code):
    cur.execute('select cat_code from es')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select * from es where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        print(myresult)
    else:
        print('sorry product is not available rightnow!')

def p2(cat_code):
    cur.execute('select cat_code from jeans')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select final_price from jeans where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        myresult=list(map(lambda x:x[0],myresult))
        print(myresult)
        syn1=('select description from jeans where cat_code=%s')
        user=cat_code
        cur.execute(syn1,user)
        myresult1=cur.fetchall()
        myresult1=list(map(lambda x:x[0],myresult1))
        print(myresult1)
        print('yes or no')
        ch=input('Enter:')
        if ch=='yes':
            a.append(myresult)
            b.append(myresult1)
            print(a)
            print(b)
            i=list(map(lambda x: x[0],a))
            j=list(map(lambda x: x[0],b))
            dicts=dict(zip(i,j))
            print('Item is added to cart')
        elif ch=='no':
            print('Do you like to complete the order?')
            ch=input('enter:')
            for letter in ch:
                if letter =='yes':
                    break

            print('Thankyou for your visit sir!')
            
    else:
        print('sorry product is not available rightnow!')
        
def jeans(cat_code):
    cur.execute('select cat_code from jeans')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select * from jeans where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        print(myresult)
    else:
        print('sorry product is not available rightnow!')
        

        
def p3(cat_code):
    cur.execute('select cat_code from tops')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select final_price from tops where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        myresult=list(map(lambda x:x[0],myresult))
        print(myresult)
        syn1=('select description from tops where cat_code=%s')
        user=cat_code
        cur.execute(syn1,user)
        myresult1=cur.fetchall()
        myresult1=list(map(lambda x:x[0],myresult1))
        print(myresult1)
        print('yes or no')
        ch=input('Enter:')
        if ch=='yes':
            a.append(myresult)
            b.append(myresult1)
            print(a)
            print(b)
            i=list(map(lambda x: x[0],a))
            j=list(map(lambda x: x[0],b))
            dicts=dict(zip(i,j))
            print(dicts)
            print('Item is added to cart')
        elif ch=='no':
            print('Do you like to complete the order?')
            ch=input('enter:')
            if ch=='yes':
                add(a)
                
                
            
            
    else:
        print('sorry product is not available rightnow!')
        
def tops(cat_code):
    cur.execute('select cat_code from tops')
    myresult1=cur.fetchall()
    myresult=list(map(lambda x : x[0],myresult1))
    if cat_code in myresult:
        syn=('select * from tops where cat_code=%s')
        user=cat_code
        cur.execute(syn,user)
        myresult=cur.fetchall()
        print(myresult)
    else:
        print('sorry product is not available rightnow!')
def add(a):
    c=0
    for p in a:
        c+=p[0]
    print(c)
        
        
a=[]
b=[]

        
while True:
    print('For Ethnic wear please enter 1:')
    print('For Western wear please enter 2: ')
    choice=int(input('please select your category:'))
    
    
    
    if choice==1:
        print('categories available are Ethnic & kurtis''\n')
        ch=input('''Select your variety in Ethnic & kurtis:a.Kurtas & kurtis,b.Ethnic sets:''')
        if ch=='a':
            cat_code=input('enter the cat_code:')
            kk(cat_code)
            p(cat_code)
            
            
            
        elif ch=='b':
            cat_code=input('enter the cat_code')
            es(cat_code)
            p1(cat_code)
        else:
            print('not available')
    elif choice==2:
        ch=input('''select your variety in western wear:jeans,tops:''')
        if ch=='jeans':
            cat_code=input('enter the cat_code:')
            jeans(cat_code)
            p2(cat_code)
        elif ch=='tops':
            cat_code=input('enter the cat_code:')
            tops(cat_code)
            p3(cat_code)
        else:
            print('not available')
