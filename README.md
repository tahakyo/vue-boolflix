# Vue Boolflix

This is a simple web application built with Vue.js that allows users to search for movies and TV shows using the TMDb API. It provides an interface similar to Netflix, where users can view popular movies, search for specific titles, and get detailed information about each title.

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/tahakyo/vue-boolflix.git
   ```

2. Install the dependencies:

   ```bash
   cd vue-boolflix
   npm install
   ```

3. Obtain an API key from [The Movie Database (TMDb)](https://www.themoviedb.org/) by creating an account.

4. Create a `.env.local` file in the project root directory and add your TMDb API key:

   ```bash
   VUE_APP_API_KEY=YOUR_API_KEY
   ```

5. Start the development server:

   ```bash
   npm run serve
   ```

6. Open http://localhost:8080 in your browser to view the application.

## Usage

The application homepage displays popular movies and TV shows. Users can search for specific titles by entering keywords in the search bar and hitting Enter or clicking the search button.

Each movie or TV show card displays the title, year, rating, and a short overview. Clicking on a card will open a modal with more detailed information about the selected title, including the full overview and the cast.

## Technologies Used

- Vue.js (Vue CLI)
- Vuex
- Vue Router
- Axios
- Bootstrap

## Screenshots

![Screenshot 1](screenshots/screenshot1.png)

![Screenshot 2](screenshots/screenshot2.png)

## Future Improvements

- Implement pagination for search results
- Add sorting and filtering options for search results
- Add more information and details about each title
- Improve styling and user interface design

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
