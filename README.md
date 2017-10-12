# Intro-Playground

Some simple exercises to practice working with Swift.

**Tip:** To render the comments as rich markup Editor > Show Rendered Markup


### Finished Classes

```swift 

class Item {
  
  let name: String!
  let price: Float!
  
  init(name: String, price: Float) {
    self.name = name
    self.price = price
  }
  
}


class Basket {
  
  var items = [Item]()
  
  func addItem(values: [Item]) {
    for value in values {
      items.append(value)
    }
  }

  func totalPrice() -> Float {
    
    var total: Float = 0
    
    for item in items {
      total = total + item.price
    }
    
    return total
  }
  
  func empty() {
    items.removeAll()
  }
  
}


var myBasket = Basket()

let itemOne = Item(name: "Phone", price: 499)
let itemTwo = Item(name: "Drink", price: 1.49)

myBasket.addItem(values: [itemOne, itemTwo])

myBasket.totalPrice()

myBasket.empty()

myBasket.totalPrice()

```
