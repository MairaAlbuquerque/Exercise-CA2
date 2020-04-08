# Exercise-CA2
Shopping Basket in Python

products = {'desc': {'suitcase', 't-shirt', 'trousers'}
            'seller': {'Paul', 'Maira', 'Mayank'}
            'price':{'suitace':50, 't-shirt':2, 'trousers':15} # Price based in EURO
            'curr': {'EUR':1, 'USD':1.23, 'BRL': 5.4}}

class Basket:
    def __init__(self):
        self.__shoppingBasket = {}
    def add_item(self, sku, qty):
        self.__shoppingBasket[sku]=self.getBasket(sku)+qty
    def remove_item(self, sku, qty):
        self.__shoppingBasket[sku]=self.getBasket(sku)-qty
    def getBasket(self, sku):
        if sku not in self.__shoppingBasket:
            return 0
        return self.__shoppingBasket[sku]
    def value(self):
        total = 0
        for k,v in self.__shoppingBasket.items():
            total+=v*products['price']
            return total
    
        
p=Basket()
p.add_item('suitcase', 1)

p.getBasket('suitcase')

p.getBasket('t-shirt')
