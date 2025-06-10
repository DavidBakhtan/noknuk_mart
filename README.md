## Project info

### **1. Home (`/`)**
- Landing page introducing the storefront and highlighting featured products or categories.
- Quick access to main sections: Products, About, Contact.

### **2. Products (`/products`)**
- Displays all products fetched from the database.
- Users can search, filter, and add products directly to their cart.

### **3. Product Detail (`/products/:id`)**
- Shows full product details: name, price (including any discount), image, description, and category.
- Option to add item directly to cart.

### **4. Cart**
- Shows a modal/dropdown or dedicated page listing all added products.
- Users can update quantities or remove products.
- Cart total updates automatically, including discount calculation.

### **5. About (`/about`)**
- Provides information about the business/brand and its mission.

### **6. Contact (`/contact`)**
- Contact form or details for reaching out to the business (e.g., email, phone, address).

### **7. Admin Panel (`/admin`)**
- **Login required** (optional, recommended for production).
- Admins can:
  - Add new products (sent to MySQL via PHP backend).
  - Edit or delete products.
  - Set or update discounts on any product.
  - All changes reflected instantly in the storefront.

---

## **Data Model (Database Structure)**

**MySQL Tables:**

- **products**
  - id (INT, PRIMARY KEY, AUTO_INCREMENT)
  - name (VARCHAR)
  - price (FLOAT)
  - image (VARCHAR)
  - description (TEXT)
  - category (VARCHAR)
  - discount (FLOAT, NULLABLE)

- **users** (for admin login, if implemented)
  - id (INT, PRIMARY KEY, AUTO_INCREMENT)
  - username (VARCHAR)
  - password (HASHED VARCHAR)

- **cart** (session-based or per user, managed client-side)

---

## **How to Use**

### **User Journey**
1. Browse or search products on the Home/Products page.
2. Click any product for more details.
3. Add products to your shopping cart.
4. View and update your cart at any time.
5. Proceed to checkout (implementation optional).

### **Admin Journey**
1. Navigate to the `/admin` panel (login if required).
2. Add new products by filling in the form (name, price, image, description, category, discount).
3. Edit or delete products as needed.
4. Set discounts directly in the admin panel; customers instantly see updated pricing.

---

## **Component Breakdown**

- **Header/Footer:** Persistent navigation, cart summary.
- **ProductCard:** Shows brief info, add-to-cart button.
- **ProductDetail:** Expanded info, add-to-cart from detail view.
- **CartDropdown:** Lists cart items, updates totals, and handles removal/updating.
- **AdminForm/AdminPanel:** For product and discount management.
- **Contexts/CartContext:** Handles all cart logic and state.

---

## **Future Improvements**
- Full authentication (for admin and customer accounts).
- Order processing and order history.
- Payment gateway integration.
- Product search and advanced filtering.

---

## **Contact**
For support or feature requests, please contact [davidbakhtan@gmail.com].
