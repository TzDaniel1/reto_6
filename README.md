1. Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/FRvCmpxx/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+funcionpara cacular el area superficial y el volumen

```
pi = 3.141592653589793

def area_total_esfera_y_cono(r1, r2, h):
    area_esfera = 4 * pi * r1**2
    lado_cono = (r2**2 + h**2)**0.5
    area_cono = pi * r2 * lado_cono + pi * r2**2
    return area_esfera + area_cono

def volumen_total_esfera_cono(r1, r2, h):
    volumen_esfera = (4/3) * pi * r1**3
    volumen_cono = (1/3) * pi * r2**2 * h    
    return volumen_esfera + volumen_cono
```

+funciones en python

```
def area_total_esfera_y_cono(r1, r2, h):
    area_esfera = 4 * pi * r1**2
    lado_cono = (r2**2 + h**2)**0.5
    area_cono = pi * r2 * lado_cono + pi * r2**2
    return area_esfera + area_cono

def volumen_total_esfera_cono(r1, r2, h):
    volumen_esfera = (4/3) * pi * r1**3
    volumen_cono = (1/3) * pi * r2**2 * h    
    return volumen_esfera + volumen_cono

if __name__ == "__main__":
  pi = 3.141592653589793
  r1 = float(input("Ingresa el radio de la esfera (r1): "))
  r2 = float(input("Ingresa el radio del cono (r2): "))
  h = float(input("Ingresa la altura del cono (h): "))
  AreaTotal = area_total_esfera_y_cono(r1, r2, h)
  VolumenTotal = volumen_total_esfera_cono(r1, r2, h)

print(f"el volumen total es: {VolumenTotal}")
print(f"el area total es: {AreaTotal}")
```

+ahora con import math, math.pi
```
import math

def area_total_esfera_y_cono(r1, r2, h):
    area_esfera = 4 * math.pi * r1**2
    lado_cono = (r2**2 + h**2)**0.5
    area_cono = math.pi * r2 * lado_cono + math.pi * r2**2
    return area_esfera + area_cono

def volumen_total_esfera_cono(r1, r2, h):
    volumen_esfera = (4/3) * math.pi * r1**3
    volumen_cono = (1/3) * math.pi * r2**2 * h    
    return volumen_esfera + volumen_cono

if __name__ == "__main__":
    r1 = float(input("Ingresa el radio de la esfera (r1): "))
    r2 = float(input("Ingresa el radio del cono (r2): "))
    h = float(input("Ingresa la altura del cono (h): "))
    AreaTotal = area_total_esfera_y_cono(r1, r2, h)
    VolumenTotal = volumen_total_esfera_cono(r1, r2, h)

    print(f"El volumen total es: {VolumenTotal}")
    print(f"El área total es: {AreaTotal}")
```

2. Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/1t4MrzsL/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+ Una función matemática para calcular el área y el perimetro.

```
pi = 3.141592653589793

def calcular_area_perimetro_cilindro(radio, altura):
    area_base = pi * radio**2
    perimetro_base = 2 * pi * radio
    area_lateral = 2 * pi * radio * altura

    area_total = 2 * area_base + area_lateral
    perimetro_total = perimetro_base

    return area_total, perimetro_total
```

+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado `r`, `a` y `b`.
```
def calcular_area_perimetro_cilindro(r, a, b):
    area_base = b * r
    perimetro_base = 2 * b + 2 * r
    area_lateral = 2 * a * perimetro_base

    area_total = 2 * area_base + area_lateral
    perimetro_total = perimetro_base

    return area_total, perimetro_total

area, perimetro = calcular_area_perimetro_cilindro(r, a, b)

if __name__ == "__main__":
  r = float(input("Ingresa el radio del cilindro (r): "))
  a = float(input("Ingresa la altura del cilindro (a): "))
  b = float(input("Ingresa la base del cilindro (b): "))

print(f"El área total del cilindro es: {area}")
print(f"El perímetro de la base del cilindro es: {perimetro}")
```

+ Revise como utilizar el valor de `pi` usando *import math* y *math.pi*
```
import math

def calcular_area_perimetro_cilindro(r, a, b):
    area_base = b * r
    perimetro_base = 2 * b + 2 * r
    area_lateral = 2 * a * perimetro_base

    area_total = 2 * area_base + area_lateral
    perimetro_total = perimetro_base

    return area_total, perimetro_total

if __name__ == "__main__":
    r = float(input("Ingresa el radio del cilindro (r): "))
    a = float(input("Ingresa la altura del cilindro (a): "))
    b = float(input("Ingresa la base del cilindro (b): "))

    area, perimetro = calcular_area_perimetro_cilindro(r, a, b)
    print(f"El área total del cilindro es: {area}")
    print(f"El perímetro de la base del cilindro es: {perimetro}")
```

3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

```
def calcular_cantidad_carne_avicola(N, M, K):
    peso_gallina = 6
    peso_gallo = 7
    peso_pollito = 1

    total_carne_gallinas = N * peso_gallina
    total_carne_gallos = M * peso_gallo
    total_carne_pollitos = K * peso_pollito

    total_carne_kilos = total_carne_gallinas + total_carne_gallos + total_carne_pollitos
    return total_carne_kilos

if __name__ == "__main__":
  N = int(input("Ingresa la cantidad de gallinas: "))
  M = int(input("Ingresa la cantidad de gallos: "))
  K = int(input("Ingresa la cantidad de pollitos: "))

  cantidad_total_carne = calcular_cantidad_carne_avicola(N, M, K)
  print(f"La cantidad total de carne de aves en kilos es: {cantidad_total_carne} kg")
```

4. Mi mamá me manda a comprar P panes a 300 cada uno, M bolsas de leche a  3300 cada una y H huevos a  350 cada uno. Hacer un programa que me diga las vueltas (o lo que quedo debiendo) cuando me da un billete de B pesos.
```
def calcular_vueltas(P, precio_pan, M, precio_leche, H, precio_huevo, B):
    total_compra = P * precio_pan + M * precio_leche + H * precio_huevo
    vueltas = B - total_compra
    return vueltas

precio_pan = 300
precio_leche = 3300
precio_huevo = 350

if __name__ == "__main__":
  P = int(input("Ingresa la cantidad de panes a comprar: "))
  M = int(input("Ingresa la cantidad de bolsas de leche a comprar: "))
  H = int(input("Ingresa la cantidad de huevos a comprar: "))
  B = float(input("Ingresa la cantidad de dinero entregada: "))

  vueltas = calcular_vueltas(P, precio_pan, M, precio_leche, H, precio_huevo, B)

if vueltas >= 0:
    print(f"Las vueltas son: {vueltas} pesos")
else:
    print(f"Queda debiendo: {abs(vueltas)} pesos")
```
5. Haga un programa que utilice una función para calcular el valor de un préstamo `C` usando interés compuesto del `i` por `n` meses.
```
def calcular_monto_compuesto(C, i, n):
    M = C * (1 + i/100)**n
    return M

if __name__ == "__main__":
  C = float(input("Ingresa el capital inicial (préstamo) en pesos: "))
  i = float(input("Ingresa la tasa de interés anual en porcentaje: "))
  n = int(input("Ingresa el número de meses del préstamo: "))

  monto_total = calcular_monto_compuesto(C, i, n)
  print(f"El monto total al final de {n} meses es: {monto_total} pesos")
```

6. El número de contagiados de Covid-19 en el país de NuncaLandia se duplica cada día. Hacer un programa que diga el número total de personas que se han contagiado cuando pasen D días a partir de hoy, si el número de contagiados actuales es C.
```
def calcular_contagiados_totales(C, D):
    contagiados_totales = C * 2**D
    return contagiados_totales

if __name__ == "__main__":
    C = int(input("Ingresa el número de contagiados actuales en NuncaLandia: "))
    D = int(input("Ingresa el número de días a partir de hoy: "))

    contagiados_totales = calcular_contagiados_totales(C, D)
    print(f"El número total de contagiados en NuncaLandia después de {D} días será: {contagiados_totales}")
```
