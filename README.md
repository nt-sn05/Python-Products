### 1. Active productlarni olish

**Requirement:**

* `is_active == True`

**Focus:**

* filtering basics

---

### 2. Product nomlari listini chiqarish

**Output:**

```python
["iPhone 15", "Sneakers", ...]
```

**Focus:**

* mapping

---

### 3. Productlar sonini hisoblash

**Focus:**

* aggregation (len)

---

### 4. Har bir productdagi variantlar soni

**Output:**

```python
{
  "product_id": 3
}
```

**Focus:**

* nested list bilan ishlash

---

### 5. Out-of-stock variantlarni topish

**Condition:**

```python
stock == 0
```

**Focus:**

* deep traversal

---

### 6. Barcha review ratinglarni bitta listga yig‘ish

**Output:**

```python
[5, 4, 3, 5, 2, ...]
```

**Focus:**

* flatten

---

### 7. Eng arzon variantni topish (global)

**Output:**

* minimal price variant

**Focus:**

* min + nested iteration

---

### 8. Har bir product uchun average rating hisoblash

**Edge case:**

* reviews yo‘q bo‘lsa → `None` yoki `0`

**Focus:**

* aggregation + defensive coding

---

### 9. Eng qimmat variant (per product)

**Output:**

```python
{
  "product_id": max_price
}
```

**Focus:**

* per-entity computation

---

### 10. Category bo‘yicha group qilish

**Output:**

```python
{
  "Electronics": [...],
  "Clothing": [...]
}
```

**Focus:**

* grouping logic

---

### 11. Price range filter (variant-based)

**Requirement:**

* agar *kamida bitta variant* price range ichida bo‘lsa → product qaytadi

**Focus:**

* any() pattern
* real ecommerce logic

---

### 12. Search (case-insensitive)

**Requirement:**

```python
query = "iphone"
```

**Focus:**

* string normalization (`lower()`)

---

### 13. Flatten variants (analytics format)

**Output:**

```python
[
  {
    "product_id": ...,
    "variant_id": ...,
    "price": ...,
    "stock": ...
  }
]
```

**Focus:**

* denormalization

---

### 14. Top N products by rating

**Requirement:**

* avg rating bo‘yicha sort
* `top_n=3`

**Focus:**

* sorting + computed fields

---

### 15. Low stock alert system

**Condition:**

```python
stock < 5
```

**Output:**

* alert list (product + variant info)

**Focus:**

* real inventory logic
