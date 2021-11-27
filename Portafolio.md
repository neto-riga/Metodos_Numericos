<div class="img-container">
<center>
<img src="escudo-d.png"
     alt="Logo"
     style="width:200px; text-align:"center";" />
</center>
</div>
<br><br>

# Portafolio Métodos Numéricos :technologist:
<center>Rivera Gálvez Ernesto</center>

<br> <br>
# Índice

- [Portafolio Métodos Numéricos :technologist:](#portafolio-métodos-numéricos-technologist)
- [Índice](#índice)
- [Análisis de Error](#análisis-de-error)
  - [Ejercicio 1. Error de Redondeo](#ejercicio-1-error-de-redondeo)
- [Solución de Ecuaciones](#solución-de-ecuaciones)
  - [Ejercicio 2. Método de Bisección](#ejercicio-2-método-de-bisección)
  - [Ejercicio 3. Método de la Posición Falsa](#ejercicio-3-método-de-la-posición-falsa)
  - [Ejercicio 4. Método de Newton](#ejercicio-4-método-de-newton)
  - [Ejercicio 5. Método de la Secante](#ejercicio-5-método-de-la-secante)
  - [Ejercicio 6. Método de Bairstow](#ejercicio-6-método-de-bairstow)
- [Sistemas de Ecuaciones Lineales](#sistemas-de-ecuaciones-lineales)
  - [Ejercicio 6. Inversa/Determinante](#ejercicio-6-inversadeterminante)
  - [Ejercicio 7. Método de Gauss](#ejercicio-7-método-de-gauss)
  - [Ejercicio 8. Método de Intercambio](#ejercicio-8-método-de-intercambio)
  - [Ejercicio 9. Matrices Particionadas](#ejercicio-9-matrices-particionadas)
  - [Ejercicio 10. Método de Jácobi](#ejercicio-10-método-de-jácobi)
  - [Ejercicio 11. Método de Gauss-Seidel](#ejercicio-11-método-de-gauss-seidel)
  - [Ejercicio 12. Método de Relajación](#ejercicio-12-método-de-relajación)
- [Factorización de Matrices](#factorización-de-matrices)
  - [Ejercicio 13. Método de Doolittle](#ejercicio-13-método-de-doolittle)
  - [Ejercicio 14. Método de Cholesky y Crout](#ejercicio-14-método-de-cholesky-y-crout)
- [Obtención de Valores Propios](#obtención-de-valores-propios)
  - [Ejercicio 15. Método de Potencias](#ejercicio-15-método-de-potencias)
  - [Ejercicio 16. Transformación de Hausholder](#ejercicio-16-transformación-de-hausholder)
  - [Ejercicio 17. Iteración QR](#ejercicio-17-iteración-qr)

# Análisis de Error

## Ejercicio 1. Error de Redondeo
[Índice](#índice)

# Solución de Ecuaciones

## Ejercicio 2. Método de Bisección
[Índice](#índice)

Determina el coeficiente de rozamiento c, necesario para que un paracaidista de masa *m* = 68.1 tenga una velocidad de 40 $m/s$ después de una caída libre de *t* = 10s. La aceleración de la gravedad es de 9.8 $m/s^2$.

Este problema se puede resolver determinando la raíz de la ecuación:

$$ f(c) =\frac{gm}{c}\left(1-e^{-\left(\frac{c}{m}\right)t}\right)-v $$

(Segunda Ley de Newton)
Donde: 



> *t* = tiempo

> *v* = velocidad

> *m* = masa


> *g* = aceleración de la gravedad

<br>

$
f(c) =\frac{(9.8)(68.1)}{c}\left(1-e^{-\left(\frac{c}{68.1}\right)10}\right)-40
$
 

Resolver el problema, elegir un intervalo,
encontrar una raíz, con tolerancia 0.00005 en el error relativo.

Ahora implementamos el método de la bisección. Colocamos la tolerancia del error en la condicion del *while* para realizar el proceso hasta que se compla. Para que el método funcione, verificamos $f(a)*f(b)<0$ Es decir, que tengan signos contrarios.  Si se cumple, entonces $b\leftarrow	p$ $a\leftarrow	 a$ De lo contrario $a\leftarrow	 p$ $b \leftarrow	 b$ Obtenemos el punto medio para que, de ser necesario repitamos el proceso.

$p = \frac{a+b}{2}$ Adjuntamos a *p* nuestra lista de soluciones además de contar las iteraciones. Calculamos el *error relativo*, el cual será utilizado como criterio para detener el método. $E_{a}=|x_{n}-x_{n-1}|$ Obtenemos también el *error relativo*  $E_{r}=\frac{|x_{n}-x_{n-1}|}{|x_{n}|}$ Realizamos el conteo de la iteraciones realizadas y guardamos los errores calculados.

El programa utilizado para implementar el método se concentra en el siguiente código.

```python
a = [14.0]
b = [16.0]
p = (a[0]+b[0])/2
solucion = [p]
err_abs = ['NA']
i=int(0)
iteraciones = [i]
err_rel = [1.0]

while(err_rel[i]>0.00005):
    if (f(a[i])*f(solucion[i]))<0:
        a.append(a[i])
        b.append(p)
    else:
        a.append(p)
        b.append(b[i])
    
    i+=1
    p = (a[i]+b[i])/2
    solucion.append(p)
    err_abs.append(abs(solucion[i]-solucion[i-1]))
    err_rel.append( abs(solucion[i]-solucion[i-1])/abs(solucion[i]) )
    iteraciones.append(i)
    
err_rel[0]='NA'
```

## Ejercicio 3. Método de la Posición Falsa
[Índice](#índice)
## Ejercicio 4. Método de Newton
[Índice](#índice)
## Ejercicio 5. Método de la Secante
[Índice](#índice)
## Ejercicio 6. Método de Bairstow
[Índice](#índice)

# Sistemas de Ecuaciones Lineales

## Ejercicio 6. Inversa/Determinante
[Índice](#índice)
## Ejercicio 7. Método de Gauss
[Índice](#índice)
## Ejercicio 8. Método de Intercambio
[Índice](#índice)
## Ejercicio 9. Matrices Particionadas
[Índice](#índice)
## Ejercicio 10. Método de Jácobi
[Índice](#índice)
## Ejercicio 11. Método de Gauss-Seidel
[Índice](#índice)
## Ejercicio 12. Método de Relajación
[Índice](#índice)

# Factorización de Matrices

## Ejercicio 13. Método de Doolittle
[Índice](#índice)
## Ejercicio 14. Método de Cholesky y Crout
[Índice](#índice)

# Obtención de Valores Propios


## Ejercicio 15. Método de Potencias
[Índice](#índice)
## Ejercicio 16. Transformación de Hausholder 
[Índice](#índice)
## Ejercicio 17. Iteración QR
[Índice](#índice)