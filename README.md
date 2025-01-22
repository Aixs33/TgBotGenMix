# Hookah Mix Generator Telegram Bot

This project implements a Telegram bot for creating custom hookah mixes. Users can interact with the bot to select tobacco, flavors, and strengths, generating unique blends for their hookah sessions.

## Project Architecture

The architecture follows a clean separation of concerns:

1. **Consumer**: Responsible for fetching events and passing them to the processor.
2. **Event Processor**:
    - **Fetcher**: Retrieves events from an event source.
    - **Processor**: Processes the events and interacts with the Telegram API and storage.
3. **Client**: The client manages the communication with the Telegram API using a bot token.
4. **Telegram API**: The bot communicates with users via the Telegram platform.

## Storage

The project implements two types of storage for managing tobacco and flavor information:

- **In-memory storage**: For quick access to the current tobacco and flavor data.
- **SQLite storage**: Persistent storage for saving and retrieving data across bot sessions.

## Technologies Used

- **Telegram Bot API**: For communication with users via Telegram.
- **SQLite**: For persistent data storage.
- **Go**: The language used for backend logic, event handling, and bot management.
- **Cache**: For faster, in-memory storage operations.

## Features

- **Tobacco Management**: Add, delete, and list tobaccos.
- **Flavor Management**: Add and delete flavors for specific tobaccos, including different flavor types.
- **Mix Generation**: Generate hookah mixes based on tobacco strength and flavor type