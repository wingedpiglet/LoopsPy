import pygame
pygame.init()
pygame.display.set_caption("for loops")
screen = pygame.display.set_mode((800, 800))

while True:
    event = pygame.event.wait()
    
    if event.type == pygame.QUIT:
        break
    pygame.draw.rect(screen, (21, 156, 161), (1, 1, 800, 800))
    for i in range(10):
        for j in range(10):
            pygame.draw.rect(screen, (100, 0, 100), (i*80, j*50, 20, 20))
            pygame.draw.rect(screen, (252, 151, 252), (i*80+5, j*50+5, 10, 10))
    pygame.display.flip()
pygame.quit()
