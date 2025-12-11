# Product-Service

RESTful API for product catalog management.

## Technology Stack

- Node.js
- Express.js
- MongoDB with Mongoose

## API Endpoints

- `GET /health` - Health check
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `POST /api/products` - Create new product
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product..

## Local Development

```bash
npm install
npm start
```

For development with auto-reload:

```bash
npm run dev
```

Application will be available at http://localhost:3001

## Environment Variables

- `PORT`: Server port (default: 3001)
- `MONGODB_URI`: MongoDB connection string (default: mongodb://localhost:27017/petstore)
- `NODE_ENV`: Environment (development/production)

## Docker Build

```bash
docker build -t product-service:latest .
docker run -p 3001:3001 product-service:latest
```

## Health Check

```bash
curl http://localhost:3001/health
```

## Example API Calls

### Create Product

```bash
curl -X POST http://localhost:3001/api/products \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Dog Food Premium",
    "description": "High-quality dog food",
    "price": 29.99,
    "category": "Food",
    "stock": 100
  }'
```

### Get All Products

```bash
curl http://localhost:3001/api/products
```

### Update Product

```bash
curl -X PUT http://localhost:3001/api/products/product123 \
  -H "Content-Type: application/json" \
  -d '{
    "stock": 150
  }'
```


