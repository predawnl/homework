# homework

�����ǳ�ѧ�����Ի���һ���ܼ򵥵���
�������£�
# drawtree.py
from turtle import Turtle, mainloop
def tree(plist, l, a, f):
  if l > 5: #
    lst = []
    for p in plist:
      p.forward(l)#���ŵ�ǰ�ķ��򻭻�
      q = p.clone()
      p.left(a) 
      q.right(a)
      lst.append(p)#��Ԫ�����ӵ��б�����
      lst.append(q)
    tree(lst, l*f, a, f)
def main():
  p = Turtle()
  p.color("green")
  p.pensize(5)
  p.hideturtle() 
  p.speed(10)
  p.left(90)
  p.penup() 
  p.goto(0,-200)
  p.pendown()
  
  t = tree([p], 200, 65, 0.6375)
    
main()
