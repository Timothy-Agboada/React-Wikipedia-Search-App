## 🚀 30-Day Coding Challenge: Day 21

This project is the twenty-first entry in my 30-day coding challenge. Today's goal was to build a real-time search application that interacts with the Wikipedia API. This project focuses on advanced `useEffect` patterns for fetching data in response to live user input, including debouncing and request cancellation to ensure a robust and efficient user experience.

### 📖 Project Overview

This is a clean and responsive Wikipedia search application. As a user types into the search bar, the app waits for a brief pause and then fetches a list of relevant article suggestions from the Wikipedia API. The results, including the article title and a short description, are displayed instantly. This project is a practical demonstration of how to handle the complexities of live search functionality in a modern web application.

### ✨ Live Demo & Screenshot

Below is a screenshot of the application's interface.
![Jun-30-2025 15-51-32](https://github.com/user-attachments/assets/b6e81826-9e0a-42f3-b29d-5d5279eafbe7)


### 🌟 Key Features

* **Live Wikipedia Search:** Fetches search results in real-time from the official Wikipedia API.
* **Debounced API Requests:** Implements a `setTimeout` to "debounce" the input, ensuring API calls are only made after the user has paused typing, which improves performance and reduces network traffic.
* **Fetch Cancellation:** Uses the `AbortController` API within a `useEffect` cleanup function to cancel previous, outdated API requests. This prevents race conditions and ensures only the most recent search results are displayed.
* **Loading and No-Result States:** Provides clear UI feedback to the user when the application is fetching data or when no results are found for a given term.
* **Dynamic Results Rendering:** The search results are dynamically rendered by mapping over the data returned from the API.
* **Modern & Responsive UI:** Styled with Tailwind CSS for a clean, modern, and fully responsive layout.

### 💻 Technologies Used

This project was built using a modern, lightweight React setup.

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Babel](https://img.shields.io/badge/Babel-%23F9DC3e.svg?style=for-the-badge&logo=babel&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

* **React:** The core library for building the user interface.
* **ReactDOM:** Used to render the React component into the browser's DOM.
* **Babel:** Used as a transpiler to convert JSX into standard JavaScript.
* **Tailwind CSS:** For all styling and layout.
* **Wikipedia API:** The source for all search results.
* **Font Awesome:** For icons.

### 🛠️ How to Run Locally

This project is set up to be extremely simple to run, with no build process required:

1.  **Clone the repository (or download the code):**
    ```bash
    git clone https://github.com/timothy-agboada/react-wikipedia-search.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd react-wikipedia-search
    ```
3.  **Open the `index.html` file in your web browser.** The CDN links will handle loading all necessary libraries automatically.

No API key is required for this project.

### 🎯 Learning Objectives

This project was a crucial exercise for mastering advanced data-fetching patterns in React:

* **The `useEffect` Hook for Data Fetching:** Gaining experience with triggering side effects (API calls) in response to state changes (`searchTerm`).
* **`useEffect` Cleanup Function:** Implementing the cleanup pattern to cancel asynchronous operations. This is a critical skill for preventing bugs and memory leaks in more complex applications.
* **Using `AbortController`:** Learning the modern, standard browser API for cancelling `fetch` requests.
* **Debouncing:** Implementing a common performance optimization technique to limit the rate of function execution.
* **Handling Complex API Responses:** Parsing and formatting data from a real-world API that returns data in a non-standard JSON structure.
