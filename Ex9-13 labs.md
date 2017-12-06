```python
def matrixmulti(X, Y):
    # X dimension is M x N
    # Y dimension is N x P
    M = len(X)
    N = len(X[0])
    P = len(Y[0])
    
    # resultant matrix dimension is M x P
    result = [[0] * P  for row in range(M)]
    
    if  N != len(Y):  
        print ("Incorrect dimensions.")
        return

    for i in range(M):
        for j in range(P):
            for k in range(N):
                result[i][j] += X[i][k] * Y[k][j]

    return result
```    
```python
import sys

def wordcount(S):
    N = len(S.strip().split())
    return N



filename = sys.argv[1]
try:
   f = open(filename, 'r')
   text = f.read()
   print(wordcount(text))
   f.close()
except:
   print("File not available!")
   

```


```python
import sys
def freqWords(S):
    words = S.strip().split()    
    d = {}
    for word in words:
        if word in d:
            d[word] += 1
        else:
            d[word] = 1    
    m = max(d.values())    
    freq = []
    for word in d.keys():
        if d[word] == m:
            freq += [word]    
    return freq


filename = sys.argv[1]
try:
   print(filename)
   f = open(filename, 'r')
   text = f.read()
   print(text)
   print('freq words:', freqWords(text))
   f.close()
except:
   print("freqWords: File not available!")
   print(sys.argv)
```

```python
import sys, pygame
pygame.init()

size = width, height = 320, 240
speed = [2, 2]
black = 0, 0, 0

screen = pygame.display.set_mode(size)
clock = pygame.time.Clock()

ball = pygame.image.load("ball.gif")
ballrect = ball.get_rect()

while 1:
    clock.tick(30)	
    for event in pygame.event.get():
        if event.type == pygame.QUIT: sys.exit()

    ballrect = ballrect.move(speed)
    if ballrect.left < 0 or ballrect.right > width:
        speed[0] = -speed[0]
    if ballrect.top < 0 or ballrect.bottom > height:
        speed[1] = -speed[1]

    screen.fill(black)
    screen.blit(ball, ballrect)
    pygame.display.flip()
```


```python
import pygame
import math
import sys

pygame.init()
screen = pygame.display.set_mode( (600, 300))
clock = pygame.time.Clock()

while(True) :
	for event in pygame.event.get() :
		if event.type == pygame.QUIT:
			sys.exit()
	xRadius = 250
	yRadius = 100
	for degree in range(0,360,10) :
		x1 = int(math.cos( degree * 2 * math.pi / 360) * xRadius) + 300
		y1 = int(math.sin(degree * 2 * math.pi / 360) * yRadius) + 150
		screen.fill(( 0, 0, 0))
		pygame.draw.circle(screen, (255, 0, 0), [300, 150], 35)
		pygame.draw.ellipse(screen, (255, 255, 255), [50, 50, 500, 200], 1)
		pygame.draw.circle(screen, (0, 0, 255), [x1, y1], 15)
		pygame.display.flip()
		clock.tick(5)
```

ref: https://www.slideshare.net/DrAnurekhaR/simulate-elliptical-orbit-in-pygame

```python
import pygame
import math
import sys

pygame.init()
screen = pygame.display.set_mode( (600, 300))
clock = pygame.time.Clock()

while(True) :
        for event in pygame.event.get() :
                if event.type == pygame.QUIT:
                        sys.exit()
        xRadius = 250
        yRadius = 100
        for degree in range(0,360,10) :
                x1 = int(math.cos( degree * 2 * math.pi / 360) * xRadius) + 300
                y1 = int(math.sin(degree * 2 * math.pi / 360) * yRadius) + 150
                screen.fill(( 0, 0, 0))
                pygame.draw.circle(screen, (255, 0, 0), [300, 150], 35)
                pygame.draw.ellipse(screen, (255, 255, 255), [50, 50, 500, 200], 1)
                pygame.draw.circle(screen, (0, 0, 255), [x1, y1], 15)
                pygame.display.flip()
                clock.tick(5)
```
