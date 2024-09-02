# Image Search App

This project is a web application that allows users to search for images and view results fetched from an API. Built with React and Tailwind CSS, the app provides a smooth and responsive interface for image searching.

## Features

- **Search Images**: Enter a search term to find relevant images from an API.
- **Display Results**: View a grid of images based on the search query.
- **Responsive Design**: Optimized for various screen sizes using Tailwind CSS.

## Tech Stack

- **React**: A JavaScript library for building user interfaces.
- **Tailwind CSS**: A utility-first CSS framework for designing responsive and custom UI components.
- **PostCSS**: A tool for transforming CSS with plugins like Tailwind CSS.
- **JavaScript (JS)**: Handles the logic and API integration of the application.
- **HTML & CSS**: For structuring and styling the application.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Node.js**: JavaScript runtime.
- **npm**: Package manager that comes with Node.js.

## Installation and Setup

Follow these steps to set up and run the project locally:

### Commands

1. **Create a new folder and set up the React app**:

   ```bash
   mkdir image-search-app
   cd image-search-app
   npx create-react-app .
   ```

2. **Install Tailwind CSS and related dependencies**:

   ```bash
   npm i -D tailwindcss postcss-cli autoprefixer
   ```

3. **Initialize Tailwind CSS with a full configuration**:

   ```bash
   npx tailwind init tailwind.js --full
   ```

4. **Create the PostCSS configuration file**:

   ```bash
   touch postcss.config.js
   ```

5. **Start the development server**:

   ```bash
   npm run start
   ```

### Make Changes

1. **Update `package.json`**:

   In your `package.json`, modify the `scripts` section to include CSS build and watch commands:

   ```json
   "scripts": {
     "start": "npm run watch:css && react-scripts start",
     "build": "npm run build:css && react-scripts build",
     "test": "react-scripts test",
     "eject": "react-scripts eject",
     "build:css": "postcss src/assets/tailwind.css -o src/assets/main.css",
     "watch:css": "postcss src/assets/tailwind.css -o src/assets/main.css"
   }
   ```

2. **Configure Tailwind in your project**:

   - Ensure `tailwind.css` is properly set up in `src/assets`.
   - Tailwind directives should be added in your CSS file:

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

## Usage

1. **Search for Images**: Enter keywords into the search bar to find images.
2. **View Results**: The images related to your search query will be displayed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Tailwind CSS for making responsive design easier.
- React for the UI components.
