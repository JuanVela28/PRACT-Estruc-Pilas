# PRACT-Estruc-Pilas
Juan Carlos Vela Mena. 3SB.

class Pila:
    def __init__(self, capacidadM):
        self.pila = []
        self.capacidadM = capacidadM
        self.tope = 0

    def pilaVacía(self):
        return self.tope == 0

    def pilaLlena(self):
        return self.tope == self.capacidadM

    def añadirDatos(self, dato):
        if self.pilaLlena():
            print("La pila está llena, no se pueden añadir más datos.")
            return
        self.pila.append(dato)
        self.tope += 1
        self.mostrar_pila()

    def eliminarDatos(self):
        if self.pilaVacía():
            print("La pila está vacía, no hay datos que eliminar.")
            return
        datos = self.pila.pop()
        self.tope -= 1
        self.mostrar_pila()

    def mostrar_pila(self):
        print("Pila:", self.pila)

pila = Pila(8)

pila.añadirDatos("X")
pila.añadirDatos("Y")
pila.eliminarDatos()
pila.eliminarDatos()
pila.eliminarDatos()
pila.añadirDatos("V")
pila.añadirDatos("W")
pila.eliminarDatos()
pila.añadirDatos("R")

# ¿Con cuántos elementos quedó la pila?: La pila terminó con 2 elementos.
# ¿Hubo algún caso de error (desbordamiento o subdesbordamiento)?: Sí, en este código hubo un caso de subdesbordamiento, ya que en unas situaciones que se querían eliminar elementos, no quedaban elementos para eliminar porque la pila se encontraba vacía así que por eso saca el mensaje "La pila está vacía, no hay datos que eliminar".
