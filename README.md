# Django React Taxi Booking App

A full-stack taxi booking web application built with a Django REST Framework backend and a React frontend. This application provides a platform for riders to book rides and for drivers to manage their rides and vehicles.

## Features

### Backend (Django)

- **User Authentication:** JWT-based authentication (Login, Signup, Token Refresh) using `simple-jwt`.
- **User Roles:** Separate models and permissions for `Riders` and `Drivers`.
- **Driver Management:**
  - Driver profile creation and management (profile picture, license documents).
  - Vehicle management (add car details, registration, insurance).
  - Driver account status (Active, Pending, Suspended).
- **Rider Management:**
  - Rider profile creation and management.
  - Save and manage multiple addresses.
- **Ride Booking & Management:**
  - Create, view, and manage ride bookings.
  - Dynamic ride pricing based on distance and duration.
  - Real-time ride status updates (Pending, Accepted, In Progress, Completed, Canceled).
- **API Documentation:** Auto-generated API schema and documentation using `drf-spectacular` (Swagger UI and ReDoc).
- **Admin Panel:** Django admin panel for managing all data models.

### Frontend (React)

- **User Authentication:** User-friendly Login and Signup forms with validation.
- **Role-based Dashboards:** Separate dashboards and navigation for Riders and Drivers.
- **Interactive Map:**
  - Map integration using `Mapbox` and `react-map-gl`.
  - Geocoding and search functionality for pickup and drop-off locations using `@mapbox/search-js-react`.
- **Ride Booking:**
  - A dedicated page for riders to book a new ride.
  - Real-time price estimation.
- **Ride Management:**
  - Riders can view their past and current bookings.
  - Drivers can view available ride requests and their ride history.
- **Responsive Design:** A responsive and modern user interface built with `Tailwind CSS`.
- **Protected Routes:** Secure routes for authenticated users and role-specific permissions.

## Technologies Used

### Backend

- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [djangorestframework-simplejwt](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/)
- [drf-spectacular](https://drf-spectacular.readthedocs.io/en/latest/)
- [django-cors-headers](https://github.com/adamchainz/django-cors-headers)

### Frontend

- [React](https://reactjs.org/)
- [Vite](https://vitejs.dev/)
- [React Router](https://reactrouter.com/)
- [Axios](https://axios-http.com/)
- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/api/)
- [React Map GL](https://visgl.github.io/react-map-gl/)
- [Tailwind CSS](https://tailwindcss.com/)

## Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+
- `pip` and `npm`

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/django-api-react-taxi-booking-app.git
    cd django-api-react-taxi-booking-app
    ```

2.  **Setup the Backend:**
    - Navigate to the `backend/taxi` directory:
      ```sh
      cd backend/taxi
      ```
    - Create a virtual environment and activate it:
      ```sh
      python -m venv venv
      source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
      ```
    - Install the required packages:
      ```sh
      pip install -r requirements.txt
      ```
    - Run the database migrations:
      ```sh
      python manage.py migrate
      ```
    - Start the Django development server:
      ```sh
      python manage.py runserver
      ```
    The backend will be running at `http://127.0.0.1:8000/`.

3.  **Setup the Frontend:**
    - Open a new terminal and navigate to the `frontend/ridebooking` directory:
      ```sh
      cd frontend/ridebooking
      ```
    - Install the required packages:
      ```sh
      npm install
      ```
    - Start the React development server:
      ```sh
      npm run dev
      ```
    The frontend will be running at `http://localhost:5173/`.

### API Documentation

Once the backend is running, you can access the API documentation at the following endpoints:
- **Swagger UI:** `http://127.0.0.1:8000/api/schema/swagger-ui/`
- **ReDoc:** `http://127.0.0.1:8000/api/schema/redoc/`

## Project Structure

```
django-api-react-taxi-booking-app/
├── backend/
│   └── taxi/           # Django project
│       ├── app_settings/ # Django app for site settings
│       ├── authapp/      # Django app for user authentication
│       ├── drivers/      # Django app for drivers
│       ├── riders/       # Django app for riders
│       ├── rides/        # Django app for rides
│       └── taxi/         # Django project settings
└── frontend/
    └── ridebooking/    # React project
        ├── src/
        │   ├── api/
        │   ├── assets/
        │   ├── components/
        │   ├── context/
        │   ├── permissions/
        │   └── routes/
        └── ...
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have any suggestions or find any bugs.

## Software Engineer & Artificial Intelligence Expert

OGAENYI CALEB .O. (Calebisco -- GitHub)