# Bybit Trading Bot

This repository contains a Python-based trading bot that interfaces with the Bybit exchange, automating trades based on market data and predefined strategies. The bot is integrated with Telegram for notifications and supports multiple user configurations.

## Features

- **Automated Trading**: Opens and closes long/short positions on Bybit based on market signals.
- **User Management**: Handles multiple users, each with their own API keys and settings.
- **Telegram Integration**: Sends notifications via Telegram for trade actions and updates.
- **Error Handling**: Notifies users of any errors during trade execution.
- **Customizable Strategies**: Supports the customization of trading strategies.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/bybit-trading-bot.git
    cd bybit-trading-bot
    ```

2. **Install required packages**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up your API keys**:
    Replace the placeholders in the script with your actual Bybit API key and secret.

    ```python
    client = bybit.bybit(test=False, api_key="your_api_key", api_secret="your_api_secret")
    ```

4. **Configure Telegram Bot**:
    Replace the placeholder in the script with your Telegram bot token.

    ```python
    bot = telebot.TeleBot("your_telegram_bot_token")
    ```

## Usage

- **Starting the Bot**:
    Run the main script to start the bot. The bot will automatically fetch market data and execute trades based on the predefined conditions.

    ```bash
    python main.py
    ```

- **User Data Management**:
    The bot fetches and processes user data from the specified API endpoints. Ensure that the endpoints in the code are correct and accessible.

- **Trade Execution**:
    The bot opens and closes positions based on the state and position data retrieved from the APIs. It supports both long and short positions with customizable leverage.

## Configuration

### Environment Variables

- `API_KEY`: Your Bybit API key.
- `API_SECRET`: Your Bybit API secret.
- `TELEGRAM_BOT_TOKEN`: Your Telegram bot token.

### Customization

You can customize the trading strategy and bot behavior by modifying the functions in the script, such as:

- `openlong()`
- `openshort()`
- `closeposition()`

## Contributing

Contributions are welcome! Please fork this repository, make your changes, and submit a pull request.


## Disclaimer

This bot is intended for educational purposes. Use it at your own risk. Trading cryptocurrencies involves significant risk, and you should only trade with funds that you can afford to lose.
