A **visual diagram** to show the architecture, and a **code-based example** using Python (FastAPI) to represent one microservice.

---

## 📊 **Microservices Architecture Diagram**
Here’s a visual representation of a basic microservices system:

```plaintext
         +---------------------+
         |    API Gateway      |  <-- Entry point for clients
         +----------+----------+
                    |
   +----------------+--------------------+
   |                |                    |
+--v--+          +--v--+              +--v--+
| Auth|          |Product             |Order|
|Svc  |          |Service             |Service
+--+--+          +--+--+              +--+--+
   |                |                    |
   |       +--------v--------+           |
   |       |  Product DB     |           |
   |                            +--------v--------+
   |                            |  Order DB        |
+--v--+                     +---v---+
| User|                     | Email |
| DB  |                     | Svc   |
+-----+                     +-------+

All services are connected via HTTP APIs or Message Queues.
```

---

## 🧪 Code Example: Simple **Product Microservice** (Python + FastAPI)

Here’s a minimal Product Service:

```python
# product_service.py
from fastapi import FastAPI
from pydantic import BaseModel
from typing import List

app = FastAPI()

class Product(BaseModel):
    id: int
    name: str
    price: float

# Mock database
products_db = [
    Product(id=1, name="Laptop", price=999.99),
    Product(id=2, name="Phone", price=499.99)
]

@app.get("/products", response_model=List[Product])
def get_products():
    return products_db

@app.get("/products/{product_id}", response_model=Product)
def get_product(product_id: int):
    for product in products_db:
        if product.id == product_id:
            return product
    return {"error": "Product not found"}
```

### ▶️ To Run This:
```bash
uvicorn product_service:app --reload
```

Then go to: `http://localhost:8000/products`