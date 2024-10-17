```mermaid
erDiagram
    PRODUCT {
        int ProductID PK
        string ProductName
        string Size
        string Color
        float Price
    }

    CUSTOMER {
        int CustomerID PK
        string FirstName
        string LastName
        string Email
        string Phone
        string Address
    }

    SALE {
        int SaleID PK
        date SaleDate
        int CustomerID FK
        float TotalAmount
    }

    INVENTORY {
        int InventoryID PK
        int ProductID FK
        int QuantityAvailable
    }

    PRODUCT ||--o{ SALE : "sold in"
    CUSTOMER ||--o{ SALE : "makes"
    PRODUCT ||--|| INVENTORY : "contains"

```

## Documentation
The "Product" entity represents the Nike shoes sold in the store. It has the PK of ProductID. The "Customer" entity holds the customer information. It has the PK of CustomerID. The "Sale" entity links the products sold to customers. It has the PK of SaleID and the Fk of CustomerID. The "Inventory" entity tracks the available stock of each product. It has the PK of InventoryID and Fk of ProductID.

Product to Sales - Allows the store to track which products are sold.
Customer to Sale - Allows the store to track what products the customers have bought. The store can then use this information to learn the preferences of their customers and make better sales.
Product to Inventory - Allows the store to manage stock levels.