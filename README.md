##PILA SECUENCIAL

import numpy as np

class PilaSecuencial():
    __items=None
    __tope=0
    __cant=0
    
    def __init__(self, xcant):
        self.__items=np.empty(xcant,dtype=int)
        self.__cant=xcant
        self.__tope=-1
        
    def vacia(self):
        return self.__tope == -1
    
    def llena(self):
        return self.__tope == self.__cant-1
     
    def insertar(self,x):
        if(self.__tope < self.__cant-1):
            self.__tope += 1
            self.__items[self.__tope]=x
            return x
        else:
            print("Pila llena")
            
    def suprimir(self):
        if(self.vacia()):
            print("Pila Vacia")
            
        else:
            x = self.__items[self.__tope]
            self.__tope -= 1
            return x
    def mostrar(self):
        if(self.vacia()==False):
            ca=self.__tope +1
            aux=self.__tope
            for i in range(ca):
                print(self.__items[aux])
                aux-=1
        else:
            print('Vacia')
    
    def darUltimo(self):
        return self.__items[self.__tope]
        
        
        
        

