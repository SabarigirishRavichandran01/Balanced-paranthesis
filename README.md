n=input()
s=[]
a=['{','(','[']
b=['}',')',']']
f=0
for i in n:
  if i in a:
    s.append(i)
  elif i in b:
    p = b.index(i)
    print(p)
    if ((len(s) > 0) and (a[p] == s[len(s)-1])):
      s.pop()
    else:
      f=1
if len(s)==0 and f==0:
  print("Balanced")
else:
  print("Not Balanced")
