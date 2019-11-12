# homework

由于是初学，所以花了一个很简单的树
代码如下：
# drawtree.py
from turtle import Turtle, mainloop
def tree(plist, l, a, f):
  if l > 5: #
    lst = []
    for p in plist:
      p.forward(l)#沿着当前的方向画画
      q = p.clone()
      p.left(a) 
      q.right(a)
      lst.append(p)#将元素增加到列表的最后
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
