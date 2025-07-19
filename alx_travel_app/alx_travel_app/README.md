# ALX Travel App
Here's a well-structured `README.md` for your **`alx_travel_app_0x00`** Django project, tailored to match your tasks:

---

```markdown
# 🧳 alx_travel_app_0x00

A Django-based travel booking application that manages property listings, bookings, and reviews. This project includes RESTful serialization and a database seeder to populate test data.

---



---

## 🚀 Features

- 🔖 Manage **Listings** with price, location, and description.
- 📆 Handle **Bookings** by users with check-in/out dates.
- 🌟 Users can leave **Reviews** and ratings on listings.
- 🔁 Includes a custom **database seeder** using Faker.

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/alx_travel_app_0x00.git
cd alx_travel_app_0x00
````

### 2. Create a Virtual Environment

```bash
python -m venv env
env\Scripts\activate  # On Windows
# source env/bin/activate  # On Linux/macOS
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> If `requirements.txt` doesn't exist, install manually:

```bash
pip install django djangorestframework faker
```

### 4. Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

---

## 🌱 Seeding the Database

The `seed` management command uses Faker to populate sample listing data.

### Run Seeder:

```bash
python manage.py seed
```

This will add 10 sample listings with randomized data (title, location, description, and price).

---

## 📦 API Serializers

### Listings

Defined in: `listings/serializers.py`

```json
{
  "id": 1,
  "title": "Cozy Apartment in Paris",
  "location": "Paris",
  "price_per_night": 120.00,
  "description": "A great place to stay!"
}
```

### Bookings

```json
{
  "id": 1,
  "listing": 1,
  "user": 3,
  "check_in": "2025-08-01",
  "check_out": "2025-08-10",
  "guests": 2
}
```

---

## 🧪 Testing the App

```bash
python manage.py runserver
```

Visit: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## 🛠 Tech Stack

* Django
* Django REST Framework
* SQLite3 (default DB)
* Faker (for seeding)

---

## 📄 License

This project is for educational purposes and part of the **ALX Backend Specialization**.

---


