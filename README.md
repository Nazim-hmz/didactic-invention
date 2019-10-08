# didactic-invention
nb1 = int(input("Entrez le premier nombre: "))
nb2 = int(input("Entrez le deuxieme nombre: "))
if nb1 == 0:
  print(nb2)
elif nb2 == 0:
  print("Le PGCD de", "(", nb1, ";", nb2, ") est :", nb1)
else:
  def calculateur(nb1, nb2):
    nombre1 = nb1
    nombre2 = nb2
    reste = 0
    if nombre1>=nombre2:
      while nombre1-nombre2 != 0:
        reste = nombre1-nombre2
        if reste > nombre2:
          nombre1 = reste
        else:
          a = nombre2
          nombre2 = reste
          nombre1 = a
      print(nombre2)
    else:
      while nombre2-nombre1 != 0:
        reste = nombre2-nombre1
        if reste > nombre1:
          nombre2 = reste
        else:
          a = nombre1
          nombre1 = reste
          nombre2 = a
      print(nombre1)
  print("Le PGCD de", "(", nb1, ";", nb2, ") est:", end = " ")
  calculateur(nb1, nb2)
