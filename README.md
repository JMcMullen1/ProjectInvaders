# 
# Project Invaders: APM Lifecycle Quiz

A retro-style space shooter game built with p5.js that tests your knowledge of the APM (Association for Project Management) project lifecycle. This project was built as an interactive and fun way to learn key project management concepts.

![Project Invaders Gameplay](https://storage.googleapis.com/genai-assets/images/project_invaders.gif)

This application also features an AI creative partner, powered by the Google Gemini API, that allows you to modify the game's code in real-time using natural language prompts.

## Features

-   Classic space invaders-style gameplay.
-   Educational content based on the APM project lifecycle.
-   Increasing difficulty with levels and challenging boss fights every 5 levels.
-   Dynamic true/false questions that determine game progression.
-   AI-powered chat to modify the game on the fly (requires API key).
-   Responsive design that works on different screen sizes.
-   Starry space background with particle explosions for a retro feel.

## How to Play

-   **Move:** Use the `LEFT` and `RIGHT` arrow keys to move your ship.
-   **Shoot:** Press the `SPACEBAR` to shoot.
-   **Objective:** Read the question at the top of the screen. Shoot the invader (or boss weakpoint) that corresponds to the correct answer (`TRUE` or `FALSE`).
-   **Scoring:** You get points for correctly answering questions and defeating bosses.
-   **Lives:** You start with 3 lives. You lose a life if you shoot the wrong answer or get hit by an enemy bullet.

## Technology Stack

-   **Frontend:** HTML5, CSS3, TypeScript
-   **Graphics/Game Logic:** [p5.js](https://p5js.org/)
-   **UI Components:** [Lit](https://lit.dev/)
-   **AI Chat:** [Google Gemini API](https://ai.google.dev/)

## File Structure

-   `index.html`: The main entry point of the application.
-   `index.css`: Styles for the application layout, chat, and editor.
-   `index.tsx`: The main TypeScript file that initializes the game, the playground UI, and the Gemini API client.
-   `playground.tsx`: The Lit component that defines the entire UI, including the game preview, code editor, and chat interface.
-   `README.md`: This file.

## Running Locally

To run this project on your local machine:

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd <repository-directory>
    ```

2.  **Set up the API Key:**
    The AI chat functionality requires a Google Gemini API key.
    -   Get an API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    -   This project is set up to read the key from an environment variable (`process.env.API_KEY`). You will need a local development server that can handle environment variables (like Vite or Node/Express) or modify the code to include the key directly for local testing (not recommended for production).

3.  **Serve the files:**
    Since this is a simple static project, you can use any local web server. If you have VS Code, the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension is a great option.
    -   Right-click `index.html`.
    -   Select "Open with Live Server".

## Deploying to GitHub Pages

You can easily deploy a playable version of the game using GitHub Pages.

1.  **Push to GitHub:** Push your code to a new GitHub repository.

2.  **Enable GitHub Pages:**
    -   In your repository, go to `Settings` > `Pages`.
    -   Under "Build and deployment", select `Deploy from a branch` as the source.
    -   Choose the `main` branch (or whichever branch you are using) and the `/ (root)` folder.
    -   Click `Save`.

3.  **Play Online:**
    After a minute or two, your game will be live at `https://<your-username>.github.io/<your-repository-name>/`.

    **Note:** The AI chat functionality will be disabled on the public GitHub Pages version because the API key is not exposed, ensuring its security. The game itself remains fully playable.
