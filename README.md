# Pizza API Challenge

A RESTful API for managing restaurants, pizzas, and their relationships, built with Flask, SQLAlchemy, and Flask-Migrate.

## Features

- List all restaurants
- Get details for a specific restaurant
- Delete a restaurant
- List all pizzas
- Add a pizza to a restaurant
- Database migrations and seeding

## Project Structure

```
Pizza-API-Challenge/
├── config.py
├── server/
│   ├── app.py
│   ├── seed.py
│   ├── models/
│   │   ├── restaurant.py
│   │   ├── pizza.py
│   │   └── restaurant_pizza.py
│   └── controllers/
│       ├── restaurant_controller.py
│       ├── pizza_controller.py
│       └── restaurant_pizza_controller.py
```

## Setup Instructions

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd Pizza-API-Challenge
   ```

2. **Create and activate a virtual environment:**
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

4. **Set up the database:**
   ```sh
   export FLASK_APP=server/app.py
   flask db init
   flask db migrate -m "Initial migration"
   flask db upgrade
   ```

5. **Seed the database:**
   ```sh
   python -m server.seed
   ```

6. **Run the server:**
   ```sh
   flask run
   ```
   The API will be available at `http://127.0.0.1:5000/`.

## API Endpoints

### Restaurants

- `GET /restaurants`  
  List all restaurants.

- `GET /restaurants/<id>`  
  Get details for a specific restaurant.

- `DELETE /restaurants/<id>`  
  Delete a restaurant.

### Pizzas

- `GET /pizzas`  
  List all pizzas.

### Restaurant Pizzas

- `POST /restaurant_pizzas`  
  Add a pizza to a restaurant.

## License

MIT

---

**Happy coding!**
