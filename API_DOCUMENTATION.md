# Yoga Class Subscription Tracking System

A Spring Boot application for managing yoga class subscriptions, member attendance, and payments.

## Features

- Member management
- Membership type management with pricing and duration
- Subscription tracking with start/end dates
- Class attendance recording
- Payment processing and tracking
- RESTful API endpoints

## API Endpoints

### Members
- `GET /api/members/page/{page}/{size}` - Get paginated members
- `POST /api/members` - Create new member
- `GET /api/members/{id}` - Get member by ID
- `PUT /api/members/{id}` - Update member

### Membership Types
- `GET /api/membership-types` - Get all membership types
- `POST /api/membership-types` - Create membership type
- `GET /api/membership-types/{id}` - Get membership type by ID
- `PUT /api/membership-types/{id}` - Update membership type
- `GET /api/membership-types/name/{typeName}` - Get by type name
- `GET /api/membership-types/price?min={min}&max={max}` - Get by price range

### Memberships
- `GET /api/memberships` - Get all memberships
- `POST /api/memberships` - Create membership
- `GET /api/memberships/{id}` - Get membership by ID
- `PUT /api/memberships/{id}` - Update membership
- `DELETE /api/memberships/{id}` - Delete membership

### Attendance
- `GET /api/attendance` - Get all attendance records
- `POST /api/attendance` - Record attendance
- `GET /api/attendance/{id}` - Get attendance by ID
- `GET /api/attendance/member/{memberId}` - Get attendance by member

### Payments
- `GET /api/payments` - Get all payments
- `POST /api/payments` - Create payment
- `GET /api/payments/{id}` - Get payment by ID
- `GET /api/payments/membership/{membershipId}` - Get payments by membership

## Running the Application

```bash
cd springapp
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

## Sample Data

The application automatically initializes with sample data including:
- 3 membership types (Basic, Premium, Annual)
- 2 sample members
- 2 active memberships
- 2 attendance records
- 2 payment records

## Database

Uses H2 in-memory database for development. Database console available at:
`http://localhost:8080/h2-console`

Connection details:
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (empty)