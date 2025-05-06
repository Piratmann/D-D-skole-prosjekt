# D-D-skole-prosjekt
D&amp;D skole prosjekt
class Monster:
    liv=3
    enegri=20
    posisjon=[12,13,14]
    
    def __init__(self,navn):
        self.navn=navn
        print("Navnet mitt er" +self.navn)
        
    def angrip(self):
        print("Au Au!")
        self.liv -=1
        
    def sjekkLiv(self):
        if(self.liv<=0):
            print(self.navn+ " er død!")
        else:
            print(self.navn+ " har fremdeles %d liv igjen!" %self.liv)

class Drage(Monster):
    ild=50
    def flyTil(selv,posisjon):
        self.posisjon=posisjon

    def sprutIld(self,lengde):
        print(self.navn+" spruter masse ild, minst %d meter" %lengde)
        self.ild-=lengde


class KjempeBlekksprut(Monster):
    blekk=50
    def svoemTil(self,posisjon):
        self.posisjon=posisjon

    def slippBlekk(self,mengde):
        self.blekk-=mengde
        print (self.navn+" blekker! Der ble mørkt gitt...")








M1 = Monster("Uggur")
M2 = Monster("Kleis")
D1 = Drage("Katla")
BS1 = KjempeBlekksprut("Blekulf")

M1.angrip()
M1.angrip()
M2.angrip()
M1.sjekkLiv()
M1.angrip()
M1.sjekkLiv()
M2.sjekkLiv()
D1.sprutIld(5)
BS1.slippBlekk(10)
BS1.angrip()
BS1.sjekkLiv()



