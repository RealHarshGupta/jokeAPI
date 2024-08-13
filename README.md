# jokeAPI
jokeAPI , a backend project , RESTful api.
Here's a GitHub README file for your **JokeAPI** backend API project:

---

# JokeAPI

JokeAPI is a RESTful API that allows users to retrieve, create, update, and delete jokes. The API supports a variety of joke types and provides endpoints for filtering jokes based on their type.

## Features

- **Get a Random Joke:** Fetch a randomly selected joke.
- **Get a Specific Joke:** Retrieve a joke by its ID.
- **Filter Jokes:** Retrieve jokes filtered by type.
- **Create a New Joke:** Add a new joke to the collection.
- **Update an Existing Joke:** Fully replace or partially update an existing joke.
- **Delete a Specific Joke:** Remove a joke by its ID.
- **Delete All Jokes:** Clear the entire joke collection (requires authorization).

## Endpoints

1. **GET /random**
   - Returns a random joke from the collection.

2. **GET /jokes/:id**
   - Retrieves a specific joke by its ID.

3. **GET /filter**
   - Retrieves jokes filtered by their type.
   - Query Parameter: `type` (e.g., `/filter?type=Science`)

4. **POST /jokes**
   - Adds a new joke to the collection.
   - Body Parameters:
     - `text` (string): The joke content.
     - `type` (string): The category/type of the joke.

5. **PUT /jokes/:id**
   - Replaces an existing joke entirely.
   - Body Parameters:
     - `text` (string): The new joke content.
     - `type` (string): The new category/type of the joke.

6. **PATCH /jokes/:id**
   - Partially updates an existing joke.
   - Body Parameters (optional):
     - `text` (string): The updated joke content.
     - `type` (string): The updated category/type of the joke.

7. **DELETE /jokes/:id**
   - Deletes a specific joke by its ID.

8. **DELETE /all**
   - Deletes all jokes from the collection.
   - Query Parameter: `key` (string): The master key for authorization.

## Getting Started

### Prerequisites

- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/JokeAPI.git
   ```
2. Navigate to the project directory:
   ```bash
   cd JokeAPI
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```

### Running the API

Start the server:
```bash
nodemon ./index.js
```

The API will be running on `http://localhost:3000`.

## Example Usage

- **Get a random joke:**
  ```bash
  curl http://localhost:3000/random
  ```

- **Add a new joke:**
  ```bash
  curl -X POST -d "text=Why did the chicken cross the road? To get to the other side!" -d "type=Puns" http://localhost:3000/jokes
  ```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to contribute to this project.

