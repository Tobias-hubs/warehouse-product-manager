# Warehouse Product Manager Implementation

## 📌 Overview
This PR introduces the **Warehouse Product Manager** with functionality for managing immutable `Product` entities using **Java 8 Streams**.  
All functionality is covered by unit tests with **JUnit 5**.

---

## ✅ Implemented Features

### Entities
- `Product` (Java record, immutable)
- `Category` (enum type)

### Warehouse (service)
- `addProduct(Product product)` → Validates and adds new product
- `updateProduct(String id, String name, Category category, int rating)` → Updates existing product with validation
- `getAllProducts()` → Returns a defensive copy of all products
- `getProductById(String id)` → Retrieves a product by ID or throws exception
- `getProductsByCategorySorted(Category category)` → Returns products in category, sorted A–Z by name
- `getProductsCreatedAfter(LocalDate date)` → Filters by creation date
- `getModifiedProducts()` → Returns products where `createdDate != modifiedDate`
- `getCategoriesWithProducts()` → Returns all categories with at least one product
- `countProductsInCategory(Category category)` → Counts products in a given category
- `getProductInitialsMap()` → Builds a map of product name initials and their counts
- `getTopRatedProductsThisMonth()` → Returns top-rated products created this month, sorted newest first

---

## 🧪 Testing
- Comprehensive **JUnit 5 test suite** (`WarehouseTest`)
- Each public method covered with:
  - ✅ Success case(s)
  - ❌ Failure/invalid input case(s)
- ~40 test usages ensure validation of different branches and behaviors

---

## 🎯 Result
- Codebase now includes a complete product management service
- Functionality is fully validated through unit tests
- Clean, stream-based implementations following modern Java practices

---

##
School assignment 
Linked issue [Exercise 3 – Unit testing and Functional Programming](https://github.com/fungover/exercise2025/issues/7)
