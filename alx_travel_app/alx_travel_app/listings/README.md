# 🏡 Listings App

The `listings` app manages travel property listings, user bookings, and reviews within the `alx_travel_app_0x00` Django project.

---

## 📁 Directory Structure



---

## 🔧 Models

### 1. `Listing`
Represents a travel property.

| Field           | Type        | Description                  |
|----------------|-------------|------------------------------|
| `title`        | CharField   | Name of the listing          |
| `description`  | TextField   | Detailed description         |
| `location`     | CharField   | City or location             |
| `price_per_night` | DecimalField | Price per night in USD  |
| `created_at`   | DateTimeField | Auto-set on creation       |

---

### 2. `Booking`
Connects a user to a listing.

| Field       | Type        | Description               |
|------------|-------------|---------------------------|
| `listing`  | ForeignKey  | Related listing            |
| `user`     | ForeignKey  | Django user                |
| `check_in` | DateField   | Check-in date              |
| `check_out`| DateField   | Check-out date             |
| `guests`   | Integer     | Number of guests           |

---

### 3. `Review`
Allows users to rate and review listings.

| Field      | Type        | Description                |
|------------|-------------|----------------------------|
| `listing` | ForeignKey  | Reviewed listing            |
| `user`    | ForeignKey  | Reviewer                    |
| `rating`  | Integer     | Rating (1–5)                |
| `comment` | TextField   | Written review              |
| `created_at` | DateTimeField | Auto-set on creation   |

---

## 📦 Serializers

Located in `serializers.py`:

- `ListingSerializer`
- `BookingSerializer`

These serializers enable API-based representation using Django REST Framework.

---

## 🌱 Seeder Command

Located in `management/commands/seed.py`

### Purpose:
Populates the database with 10 random listings using Faker.

### Usage:

```bash
python manage.py seed
