# 🎬 Movie Discovery App

A modern, responsive React application that allows users to browse a paginated list of movies, search by title or cast members, and view movie details. This project demonstrates robust state management with **Redux Toolkit**, API handling with **Axios** (featuring automatic fallback data), and a clean UI built with **Material UI (MUI)**.

---

## 🚀 Features

* **Paginated Movie Feed:** Seamlessly fetches movies page-by-page from an external API.
* **"Load More" Functionality:** Appends new movies to the existing list allowing for infinite-scroll style navigation without losing previous data.
* **Smart Client-Side Search:** Real-time filtering that checks both **Movie Titles** and **Cast Members**.
    * *Example:* Searching for "Robert Downey Jr." will instantly find *Avengers: Endgame*.
* **Resilient Data Handling (Fallback Mode):** If the external API fails or goes down, the app automatically switches to a built-in "Backup Data" set so the user interface never breaks.
* **Responsive Design:** Optimized for Desktops, Tablets, and Mobile devices using the Material UI Grid system.

---

## 🛠️ Tech Stack

* **Frontend Library:** [React.js (v18)](https://reactjs.org/)
* **State Management:** [Redux Toolkit](https://redux-toolkit.js.org/)
* **Routing:** [React Router DOM](https://reactrouter.com/)
* **UI Components:** [Material UI (MUI)](https://mui.com/)
* **HTTP Client:** [Axios](https://axios-http.com/)
* **Icons:** [Material Icons](https://mui.com/material-ui/material-icons/)

---

## 📂 Project Structure

```bash
src/
├── api/
│   └── movies.js          # API logic: Handles fetching from server & Backup data fallback
├── components/
│   ├── MovieCard/         # Reusable component to display individual movie poster & info
│   ├── Navbar/            # Application header and navigation
│   └── SelectorComponent/ # Reusable dropdown component
├── pages/
│   └── Home/              # Main Dashboard: Handles pagination state & rendering logic
├── slice/
│   └── movieSlice.js      # Redux Slice: Manages global movie list & search state
├── utils/
│   └── getMoviesBySearch.js # Utility: Logic for filtering movies by Title OR Cast
├── store/
│   └── index.js           # Redux Store configuration
├── App.js                 # Main Application Layout & Routing
└── index.js               # Application Entry Point


```
---

## ⚡ Getting Started

Follow these instructions to get a copy of the project running on your local machine.

### Prerequisites
* **Node.js** (v14.0.0 or higher)
* **npm** (usually comes with Node.js) or **yarn**

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/RahulV17/Mobile_App.git](https://github.com/RahulV17/Mobile_App.git)
    cd Mobile_App
    ```

2.  **Install dependencies**
    ```bash
    npm install
    # OR
    yarn install
    ```

3.  **Start the development server**
    ```bash
    npm start
    # OR
    yarn start
    ```

4.  **Open in Browser**
    The app should automatically open. If not, visit:
    `http://localhost:3000`

    ---
###  State Management (Redux)
* **`setMovies`**: Used on the initial load (Page 1) to refresh the list.
* **`addMovies`**: Used when "Load More" is clicked to append new data to the existing array.

---

## 🔮 Future Improvements

* **Server-Side Search:** Move search logic to the backend to query the entire database instead of just loaded movies.
* **Movie Details Page:** Add a dynamic route (`/movie/:id`) to view full plot summaries and extended cast lists.
* **Filter by Genre:** Add a dropdown to filter movies by Action, Drama, Comedy, etc.
* **Unit Tests:** Add Jest/React Testing Library tests for the `movieSlice` and `getMoviesBySearch` utility.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  **Fork the Project**
2.  **Create your Feature Branch**
    ```bash
    git checkout -b feature/AmazingFeature
    ```
3.  **Commit your Changes**
    ```bash
    git commit -m 'Add some AmazingFeature'
    ```
4.  **Push to the Branch**
    ```bash
    git push origin feature/AmazingFeature
    ```
5.  **Open a Pull Request**

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

---

**Developed with ❤️ using React & Redux**

