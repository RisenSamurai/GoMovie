# GoMovie

GoMovie is an ongoing project aimed at building a movie information and management platform using modern web technologies.

## Technologies Used

### Frontend
- **SvelteKit**: A framework for building optimized and dynamic web applications.
- **TailwindCSS**: A utility-first CSS framework for rapid UI development.

### Backend
- **Golang**: A statically typed, compiled programming language designed for simplicity and performance.
- **Gin**: A web framework written in Go that provides a fast and scalable API server.

### Database
- **MongoDB**: A NoSQL database known for its flexibility and scalability.

## Project Structure

- `src/`: Svelte frontend application code.
- `static/`: Static assets served by the web server.
- `server/`: Go backend server code.
- `tests/`: Testing files and configurations.

## Features

- **Movie Information**: Fetch and display detailed movie information.
- **User Authentication**: Secure user login and registration system.
- **Favorites List**: Allow users to create and manage a list of favorite movies.
- **Search Functionality**: Search for movies by title, genre, and more.

## Installation

### Prerequisites
- Node.js and npm
- Golang
- MongoDB

### Steps
1. Clone the repository:
    ```sh
    git clone https://github.com/RisenSamurai/GoMovie.git
    cd GoMovie
    ```

2. Install frontend dependencies:
    ```sh
    cd src
    npm install
    cd ..
    ```

3. Install backend dependencies:
    ```sh
    go mod tidy
    ```

4. Run the backend server:
    ```sh
    go run main.go
    ```

5. Run the frontend application:
    ```sh
    cd src
    npm run dev
    ```

## Usage

- Access the application at `http://localhost:3000`.
- Explore movie details, search for movies, and manage your favorites.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
