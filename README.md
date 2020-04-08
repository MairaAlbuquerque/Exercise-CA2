# Exercise-CA2
Shopping Basket in Python

class Basket:
    def __init__(self):
        self.__shoppingBasket = {}
    def add_item(self, sku, qty):
        if sku not in self.__shoppingBasket:
            self.__shoppingBasket[sku]=qty
        else:
            self.__shoppingBasket[sku]=self.__shoppingBasket[sku]+qty
            
    def getBasket(self, sku):
        if sku not in self.__shoppingBasket:
            return 0
        return self.__shoppingBasket[sku]
        
p=Basket()
p.add_item('suitcase', 1)

p.getBasket('suitcase')

p.getBasket('t-shirt')
