# pythongpaandclasscalculator
print('program to convert marks to gpa')
print('here we can give n number of subjects \n please make sure as per your academic requirement give the number of '
      'subjects marks  ')
print( ' subject input marks example : 89 38 78 98  -- like this ')
m  = input('enter the subject marks with spaces :-  ').split()
print('the given marks are :--\n NOTE :- please check the marks here ', m)
n = len(m)
print(' here you given', n, 'number of subjects')
for i in range(len(m)):
    if 90 <= int(m[i]) <= 100:
        m[i] = 10
    elif 80 <= int(m[i]) <= 89 :
        m[i] = 9
    elif 70 <= int(m[i]) <= 79 :
        m[i] = 8
    elif 60<= int(m[i]) <= 69 :
        m[i] = 7
    elif 50 <= int(m[i]) <= 59 :
        m[i] = 6
    elif 40 <= int(m[i]) <= 49 :
        m[i] = 5
    elif 30 <= int(m[i]) <= 39 :
        m[i] = 4
    elif 20 <= int(m[i]) <= 29 :
        m[i] = 3
    else :
        print('fail')
print('each individual subject grades are :-',m)
hc = 0
for x in range(0,len(m)):
    hc = int(hc) + int(m[x])
# print(hc)
gpa = hc/ n
print('your grade is :- ', float(gpa))
print('count of fail showing is the number of subjects failed by tyhe student')
print(' if fail is showing then student is failed in one or more subjects')
if 9 <= int(gpa) <= 10:
    print('student passed with distinction with "A+" grade')
elif 7 <= int(gpa) <= 8:
    print('student passed with first class with "A" grade')
elif 5<= int(gpa) <= 6:
    print('student passed with second class with "B" grade')
elif 4<= int(gpa) <= 5:
    print('student passed with third class with "C" grade')
elif 3 <= int(gpa) <= 4:
    print('student just passed  with "D" grade')
else :
    print('student failed')
