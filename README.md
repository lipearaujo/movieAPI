# Movie API – Streaming Platform UI

A movie and TV series discovery application inspired by streaming platforms such as Netflix. The project uses React to build a dynamic catalog interface and integrates with **The Movie Database (TMDb) API** to retrieve movie and TV show information.

## Live Demo

- **Application:** [MovieAPI](https://movie-api-nine-wheat.vercel.app/)

## Features

- **Dynamic movie catalog:** Displays movies and TV shows organized into different categories.
- **Featured title:** Selects a title from the Netflix Originals category to display in the main featured section.
- **Multiple content categories:**
  - Now Playing
  - Netflix Originals
  - Trending
  - Popular Movies
  - Comedy
  - Animation
  - Horror
  - Action and Adventure
- **Movie and TV show information:** Supports fetching detailed information using the corresponding TMDb endpoints.
- **Dynamic navigation bar:** Changes its appearance based on the page scroll position.
- **Responsive visual experience:** A dark streaming-platform-inspired interface.

## Technologies

- React 18
- JavaScript
- CSS3
- Axios
- The Movie Database (TMDb) API
- Create React App

## Architecture

The application separates API communication from the main UI components.

- `App.jsx`: Main application component, responsible for loading catalog data, managing application state, selecting the featured title, and rendering content sections.
- `services/tmdbApi.js`: Handles requests to TMDb and organizes the catalog categories.
- `services/tmdAxios.js`: Configures the Axios instance and API base URL.
- `components/`: Contains the reusable interface components, including the header, featured section, and movie rows.

## Getting Started

### Prerequisites

- Node.js
- npm
- A TMDb API key

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/lipearaujo/movieAPI.git
   ```

2. Navigate to the project directory:

   ```bash
   cd movieAPI
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Configure your TMDb API key.

   Create a `.env` file in the project root:

   ```env
   REACT_APP_TMDB_API_KEY=your_tmdb_api_key
   ```

   Make sure the API service reads the key from this environment variable rather than keeping it directly in the source code.

5. Start the development server:

   ```bash
   npm start
   ```

6. Open [http://localhost:3000](http://localhost:3000).

## API Integration

This project uses the [TMDb API](https://developer.themoviedb.org/docs) to retrieve movie and TV show data.

The API service organizes requests into different categories, using endpoints such as:

- `/movie/now_playing`
- `/discover/tv`
- `/trending/all/week`
- `/movie/popular`
- `/discover/movie`

Axios is used to centralize HTTP communication and simplify asynchronous data retrieval.

## What I Learned

Through this project, I practiced:

- Building reusable React components.
- Managing component state with `useState`.
- Handling side effects and asynchronous requests with `useEffect`.
- Integrating a third-party REST API using Axios.
- Organizing API communication into a dedicated service layer.
- Working with different API endpoints and response structures.
- Managing browser events and cleaning up event listeners.
- Building a dynamic interface inspired by real-world streaming platforms.

## Future Improvements

- Add loading and error states for API requests.
- Improve API key management through environment variables.
- Add search functionality.
- Implement movie and TV show detail pages.
- Add pagination or horizontal carousel controls.
- Improve accessibility and responsive behavior.
- Migrate the project to TypeScript.
- Add automated tests.

## Author

**Filipe Araujo**

[GitHub](https://github.com/lipearaujo)
