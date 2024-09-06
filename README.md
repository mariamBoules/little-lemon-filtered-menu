# Final Assignment: Working with Data Using React Native

## Little Lemon filtered Menu

This project is the final assignment for Meta's Coursera course, "Working with Data Using React Native." The goal of this project is to create a menu application that fetches data from a remote API and stores it in a local SQLite database. The app provides search functionality and filtering options to help users browse through the menu.

**Working with Data React Native Course Final Assignment.**  
[Link to Course](https://www.coursera.org/programs/instructors-kff6i/learn/meta-working-with-data?source=search)

## Features

- Fetches menu items from a remote API.
- Stores menu data in a local SQLite database.
- Displays the menu using a `SectionList` component, organized by categories.
- Provides a search bar for querying menu items.
- Allows filtering menu items by category.

## Project Files

### `App.js`
This file is the main entry point of the application. It handles the UI and integrates various components and functions:

- **`useState` and `useEffect` hooks** are used to manage state and fetch data on component mount.
- **`Searchbar` component** is used for searching menu items.
- **`SectionList` component** is used to display menu items categorized by sections (e.g., Appetizers, Salads, etc.).
- **Filters** are used to filter menu items by categories.
- **Debounce** is applied to the search function to reduce the number of API calls.

### `utils.js`
This file contains utility functions used in the project:

- **`getSectionListData(data)`**: Transforms raw data into the structure expected by the `SectionList` component. It groups the data by category and returns the appropriate format.
- **`useUpdateEffect(effect, dependencies)`**: A custom hook that works like `useEffect`, but skips the initial render.

### `database.js`
This file handles all database-related operations using SQLite:

- **`createTable()`**: Creates a table in the SQLite database to store menu items.
- **`getMenuItems()`**: Retrieves menu items from the database.
- **`saveMenuItems(menuItems)`**: Inserts menu items into the database.
- **`filterByQueryAndCategories(query, activeCategories)`**: Filters menu items based on the search query and active categories using SQL queries.


## Acknowledgments

This project is part of Meta's Coursera course, "Working with Data Using React Native."
