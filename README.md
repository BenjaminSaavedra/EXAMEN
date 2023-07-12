# Benjamin SAAVEDRA
import datetime
fila1=[ 1,  2,  3,  4,  5,  6,  7, 8,   9, 10]
fila2=[11, 12, 13, 14, 15, 16, 17, 18, 19, 20]
fila3=[21, 22, 23, 24, 25, 26, 27, 28, 29, 30]
fila4=[31, 32, 33, 34,35, 36, 37, 38, 39, 40]
fila5=[41, 42, 43, 44, 45, 46, 47, 48, 49, 50]
fila6=[51, 52, 53, 54, 55, 56, 57, 58, 59, 60]
fila7=[61, 62, 63, 64, 65, 66, 67, 68, 69, 70]
fila8=[71, 72, 73, 74, 75, 76, 77, 78, 79, 80]
fila9=[81, 82, 83, 84, 85, 86, 87, 88, 89, 90]
fila10=[91,92, 93, 94, 95, 96, 97, 98, 99, 100]

Asistente=[]

GASTOSTOTALES=[]


total=0

def menu ():
  print("   CREATIVOS ")
  print("1. Comprar entradas")
  print("2. Mostrar ubicaciones disponibles")
  print("3. Ver listado de asistentes")
  print("4. Mostrar ganancias totales")
  print("5. Salir")
  print("")

def cosa1 ():
  CE=int(input("Seleccione cuantas entradas desea comprar(1 u 3):\n"))
  Zw=0
  while Zw<CE:
    print("")
    print("Precios:")
    print("6. Platinum,120.000$ (Asientos del 1 al 20)")
    print("7. Gold 80.000$. (Asientos del 21 al 50)")
    print("8. Silver, $50.000. (Asientos del 51 al 100)")
    print("")
    TE=int(input("Seleccione su tipo de entrada que desea comprar:\n"))



    print("Asientos: ")
    print(fila1)
    print(fila2)
    print(fila3)
    print(fila4)
    print(fila5)
    print(fila6)
    print(fila7)
    print(fila8)
    print(fila9)
    print(fila10)
    print("")
    AE=int(input("Seleccione que asiento desea comprar:\n"))
    if AE>0 and AE<11:
      fila1[AE-1]="X"
    elif AE>10 and AE<21:
      fila2[AE-1]="X"
    elif AE>20 and AE<31:
      fila3[AE-1]="X"
    elif AE>30 and AE<41:
      fila4[AE-1]="X"
    elif AE>40 and AE<51:
      fila5[AE-1]="X"
    if AE>50 and AE<61:
      fila6[AE-1]="X"
    elif AE>60 and AE<71:
      fila7[AE-1]="X"
    elif AE>70 and AE<81:
      fila8[AE-1]="X"
    elif AE>80 and AE<91:
      fila9[AE-1]="X"
    elif AE>90 and AE<101:
      fila10[AE-1]="X"

    run=int(input("Ingrese su rut(sin puntos ni guión ni letras):\n"))
    Asistente.append(run)
    print("Acción realizada con exito :D ")

    
    




    Zw+=1

def cosa2 ():
  print("Estos son los asientos disponibles: ")
  print(fila1)
  print(fila2)
  print(fila3)
  print(fila4)
  print(fila5)
  print(fila6)
  print(fila7)
  print(fila8)
  print(fila9)
  print(fila10)
  print("")

def cosa3 ():
  print("listado de asistentes")
  alfonso=sorted(Asistente)
  print(alfonso)

def cosa4 ():

  print("Ganancias totales ")
  print("El total es: ", total)

  print("")

def cosa5 ():
  print("")
  print("Nombre: ", N)
  print("Apellido: ", a)
  fecha_actual = datetime.datetime.now().date()
  print("fecha:", fecha_actual)
  print("Has salido del sistema")
  sw=0


N=input("Ingrese su nombre: ")
a=input("Ingrese su apellido: ")
print("")


sw=1
while sw==1:
  try:
    menu()

    op=int(input("Seleccione una opción: "))
    print("")

    if op==1:
      cosa1()
      

      GASTOSTOTALES.append(total)



    if op==2:
      cosa2()

    if op==3:
      cosa3()

    if op==4:
      cosa4()

    if op==5:
      cosa5()
      sw=0
      break

  except:
    print("ERROR ERROR")

