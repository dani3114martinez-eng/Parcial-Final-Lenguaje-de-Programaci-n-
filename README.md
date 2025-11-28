#Juego de Picas y Fijas plantea el número secreto
Dig_uno=int(input("Ingresa el número a adivinar debe ser de cuatro digitos y que no se repitan entre ellos, Aquí agrega el primer digito: "))
if Dig_uno > 0 and Dig_uno <= 9:
  print("El primer digito que agregaste es",Dig_uno)
else:
  print("El digito que agregaste no esta permitido, vuelve a intentar")
Dig_dos=int(input("Ingresa segundo digito: "))
if Dig_dos > 0 and Dig_dos <= 9:
  print("El segundo digito que agregaste es",Dig_dos)
else:
  print("El digito que agregaste no esta permitido, vuelve a intentar")
Dig_tres=int(input("Ingresa el tercer digito: "))
if Dig_tres > 0 and Dig_tres <= 9:
  print("El tercer digito que agregaste es",Dig_tres)
else:
  print("El digito que agregaste no esta permitido, vuelve a intentar")
Dig_cuatro=int(input("Ingresa el cuarto digito: "))
if Dig_cuatro > 0 and Dig_cuatro <= 9:
  print("El cuarto digito que agregaste es",Dig_cuatro)
else:
  print("El digito que agregaste no esta permitido, vuelve a intentar")


numero_secreto=[Dig_uno,Dig_dos,Dig_tres,Dig_cuatro]
#Juego de Picas y Fijas - Adivina el número
while True:
  Adi_Dig_uno=int(input("Ingresa el primer digito secreto a adivinar: "))
  Adi_Dig_dos=int(input("Ingresa el segundo digito secreto a adivinar: "))
  Adi_Dig_tres=int(input("Ingresa el tercer digito secreo a adivinar: "))
  Adi_Dig_cuatro=int(input("Ingresa el cuarto digito secreto a adivinar: "))

  intentos=[Adi_Dig_uno,Adi_Dig_dos,Adi_Dig_tres,Adi_Dig_cuatro]

# Condiciones Fijas
  fijas = 0
  if Adi_Dig_uno == Dig_uno: fijas += 1
  if Adi_Dig_dos == Dig_dos: fijas += 1
  if Adi_Dig_tres == Dig_tres: fijas += 1
  if Adi_Dig_cuatro == Dig_cuatro: fijas += 1

#Condiciones Picas
  picas = 0
  for i in intentos:
    if i in numero_secreto:
      picas += 1
  picas -= fijas  # quitar fijas para obtener picas reales
  print(f"\nPicas = {picas} | Fijas = {fijas}")
  if fijas == 4:
    print("\n ¡Correcto! El número era:", numero_secreto)
    break
