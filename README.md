# Reloj_processing_24_horas
## Descripción y explicación
Este repositorio fue creado con el fin de simular un reloj, realizando así, el código necesario para el mismo. 
El cuadro 1 representa los segundos en un reloj, el fondo y el color de este cuadro cambian de forma distinta durante el transcurso de un minuto.
El cuadro 2 (morado) representa los minutos en el reloj.
El cuadro número 3 (azul) representa las horas en nuestro reloj.

## Codigo
seconds = 0
minutes = 0
hours = 0

def setup():
    size(500,500)
    
def draw():
    
    global hours
    global minutes
    global seconds
    
    background(map(second(), 0,59,0,255))
    noStroke()
    fill(map(second(),0,59,255,0))
    
    square(70, seconds, 55)
    if seconds > height:
        seconds = 0
    else:
        seconds = map(second(),0,59,0,height)
        
    fill(128, 0, 128)   
    square(210, minutes, 55)
    if minutes > height:
        minutes = 0
    else:
        minutes = map(minute(),0,59,0,height)
        
    fill(25, 25, 112)
    square( 350, hours, 55)
    if hours > height:
        hours = 0
    else:
        hours = map(hour(),0,23,0,height)
