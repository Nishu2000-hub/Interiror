classDiagram
    App <|-- HomePage
    App <|-- MenuPage
    App <|-- CartPage
    MenuPage <|-- MenuList
    MenuPage ..> CoffeeModel : uses
```mermaid
classDiagram
    class Coffee {
        +id: string
        +name: string
        +description: string
        +price: number
        +reviews: CoffeeReview[]
    }
    class CoffeeReview {
        +id: string
        +rating: number
        +text: string
    }
    Coffee "1" o-- "*" CoffeeReview : reviews
