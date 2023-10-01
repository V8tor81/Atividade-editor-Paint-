# Atividade-editor-Paint-
"""Paint, for drawing shapes.

Exercises

1. Add a color.
Pesposta ma linha 95 a linha 98
2. Complete circle.
3. Complete rectangle.
4. Complete triangle.
5. Add width parameter.
"""

from turtle import *

from freegames import vector


def line(start, end):
    """Draw line from start to end."""
    up()
    goto(start.x, start.y)
    down()
    goto(end.x, end.y)


def square(start, end):
    """Draw square from start to end."""
    up()
    goto(start.x, start.y)
    down()
    begin_fill()

    for count in range(4):
        forward(end.x - start.x)
        left(90)

    end_fill()


def circle(start, end):
    """Draw circle from start to end."""
    #modificação para formação de uma circunferência:

    pass 
    

def rectangle(start, end):
    """Draw rectangle from start to end."""
    #Modificação para formação de um retângulo:

    pass  # TODO


def triangle(start, end):
    """Draw triangle from start to end."""
    #Modificação para formação de um triângulo:
    pass  # TODO

def forma_nova(start,end):
    #Modificação para formação de uma nova figura:
    pass

def tap(x, y):
    """Store starting point or draw shape."""
    start = state['start']

    if start is None:
        state['start'] = vector(x, y)
    else:
        shape = state['shape']
        end = vector(x, y)
        shape(start, end)
        state['start'] = None


def store(key, value):
    """Store value in state at key."""
    state[key] = value
