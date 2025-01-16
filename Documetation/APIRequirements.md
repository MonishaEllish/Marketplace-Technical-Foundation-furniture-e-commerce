# API Requirements

This document outlines the key API endpoints required for our furniture e-commerce marketplace.

.............................. 1. Furniture Products API.............................................. 
# GET /furniture

Fetches all available furniture products.

Response example:
```json
[
  {
    "id": "1",
    "name": "Modern Sofa",
    "price": 999.99,
    "description": "A sleek, comfortable sofa perfect for modern living rooms",
    "category": "Living Room",
    "material": "Leather",
    "color": "Black",
    "dimensions": {
      "width": 200,
      "depth": 90,
      "height": 85
    },
    "imageUrl": "https://example.com/modern-sofa.jpg"
  },
  {
    "id": "2",
    "name": "Wooden Dining Table",
    "price": 599.99,
    "description": "A sturdy wooden dining table for family gatherings",
    "category": "Dining Room",
    "material": "Oak",
    "color": "Natural",
    "dimensions": {
      "width": 180,
      "depth": 90,
      "height": 75
    },
    "imageUrl": "https://example.com/wooden-dining-table.jpg"
  }
]


.............................. 2. Furniture Orders API................................................
## POST /orders


{
  "userId": "user123",
  "items": [
    { "id": "1", "quantity": 1 },
    { "id": "2", "quantity": 1 }
  ],
  "totalAmount": 1599.98,
  "shippingAddress": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "zipCode": "12345"
  }
}



.............................. 2. Furniture Shipment API................................................
## GET /shipment/orderId


{
  "orderId": "order123",
  "status": "in transit",
  "currentLocation": "Distribution Center",
  "estimatedDelivery": "2025-01-25T15:00:00Z"
}