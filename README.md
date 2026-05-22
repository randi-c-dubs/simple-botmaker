# simple-botmaker
Simple client-side chatbot maker with flowchart creation tool.
# Day of AI: Chatbot Playground

A lightweight, zero-dependency, no-code conversational workflow builder and simulator designed for the Day of AI initiative. Built entirely within a single standalone HTML file, this tool allows students and educators to architect branching logic pathways, visualize structures dynamically via an automated flowchart map, and test their creations in a live chat simulation.

## Features

* **Interactive Workspace:** Write bot dialogue scripts and instantly spawn branching choice options using an intuitive editor panel.
* **Live Flowchart Map:** Watch an SVG-powered flowchart diagram auto-compile your conversational logic as you build. Click any node on the map canvas to jump straight into its configuration layout.
* **Sandbox Chat Simulator:** Transition instantly to a device-simulated environment where you can test-drive your user paths, complete with automatic URL text linkification.
* **Data Portability:** Export your entire narrative architecture to a clean standalone .json schema file, or import previous builds to resume working instantly.
* **Guided Onboarding:** Features a built-in interactive tour sequence that walks first-time users through the core fundamentals of building text branches.

## Getting Started

Because the entire application is built using native web technologies and utility frameworks loaded via CDN, there are no servers to run, no packages to install, and zero setup configurations required.

1. Clone or download this repository.
2. Locate the chatbot-tool.html file.
3. Open the file in any modern web browser (such as Chrome, Safari, Edge, or Firefox).

## Understanding the Build Actions

When editing a structural node block in Build Mode, the workflow editor provides three dynamic branching tools to control the conversation:

* **Add User Response:** Generates a custom selection button for your users (e.g., "Yes", "No", "Option A"). Use this option to split your story lines into diverse paths based on user decisions.
* **Add "Next":** Creates a single, linear continuation step. This is ideal for multi-bubble dialogue blocks where the bot needs to share a lot of information sequentially without forcing a decision from the user.
* **End Conversation:** Marks the block as a terminal node. The conversational simulator will automatically display your final script text (like a goodbye message) and prompt the user with a button to start the experience over.

## Data Schema

When you click Export File, the playground compresses your entire workflow map layout into a standard JSON file tracking unique identifiers (node_xxxxxxxxx).

The object schema follows this structure:

{
  "nodes": {
    "root": {
      "id": "root",
      "title": "Welcome Greeting",
      "text": "Hi! Welcome to my custom chatbot playground.",
      "type": "message",
      "branches": [
        {
          "text": "Let's begin!",
          "targetId": "node_abc123xyz",
          "isNext": false,
          "isEnd": false
        }
      ]
    }
  }
}

## Customizing the Theme

The user interface relies on Tailwind CSS. To customize the design theme to match a specific classroom or brand identity, locate the inline tailwind.config script block inside the document <head>:
