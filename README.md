# Taskecommerceweb

## Tech Stack
- **Frontend:** React JS
- **Backend:** Node JS & Express JS
- **Database:** MongoDB

## Installation Process

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Vijay0333/Taskecommerceweb.git


# 2.  install npm packages
1. install backend packages
```bash
cd Taskecommerceweb
npm install


# 3. install frontend packages

cd client
npm install


3. go to the parent folder of mern-ecommerce & create .env for connection, JWT_SECRET, BRAINTREE_MERCHANT_ID, BRAINTREE_PUBLIC_KEY and BRAINTREE_PRIVATE_KEY.

cd Taskecommerseweb
sudo nano .env
(ctrl+x to save & nano follow instruction there)

sample code for backend .env
MONGODB_URI=YOUR_MONGODB_URI
JWT_SECRET=YOUR_JWT_SECRET
BRAINTREE_MERCHANT_ID=YOUR_BRAINTREE_MERCHANT_ID
BRAINTREE_PUBLIC_KEY=YOUR_BRAINTREE_PUBLIC_KEY
BRAINTREE_PRIVATE_KEY=YOUR_BRAINTREE_PRIVATE_KEY
create another .env file inside client directory for REACT_APP_API_URL.

4.create another .env file inside client directory for REACT_APP_API_URL.

cd Taskecommerseweb/client
sudo nano .env
sample code for frontend .env
REACT_APP_API_URL=YOUR_API_URL

Instructions:

for localhost REACT_APP_API_URL is http://localhost:5000/api but for heroku (server deployment) it will be different
note: add .env on .gitignore
for server deployment use secrets directly

5. deploy this project on your local server by using this command

cd Taskecommerseweb
npm run dev
note: both backend & frontend server will start at once with the above command.
Database Structure: (Table: columns)
categories: _id, name, createdAt, updatedAt;
orders: _id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
products: _id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
users: _id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt

# App Description:
1. user can view all products
2. user can view single product
3. user can search products and view products by category and price range
4. user can add to cart checkout products using credit card info
5. user can register & sign in
6. admin can create, edit, update & delete products
7. admin can create categories
8. admin can view ordered products
9. admin can change the status of a product (processing, shipped, delivered, etc.)
