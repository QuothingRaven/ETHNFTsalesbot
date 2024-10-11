# Ethereum NFT Sales Bot

This bot monitors a specified Ethereum NFT collection for sales and sends notifications to a Discord channel when a sale occurs.

## Features

- Monitors a specific NFT contract for Transfer events (sales)
- Retrieves transaction details for each sale
- Attempts to identify the marketplace where the sale occurred
- Sends detailed notifications to a Discord channel, including:
  - Token ID
  - Buyer's address
  - Seller's address
  - Marketplace name
  - Transaction link (Etherscan)
  - NFT link (OpenSea)

## Prerequisites

- Python 3.7 or higher
- An Infura account (for Ethereum node access)
- A Discord webhook URL

## Installation

1. Clone this repository or download the script files.

2. Install the required Python packages:

   ```
   pip install -r requirements.txt
   ```

## Configuration

1. Open the `nft_sales_bot.py` file and replace the following placeholders with your actual values:

   - `YOUR_INFURA_PROJECT_ID`: Your Infura project ID
   - `YOUR_NFT_CONTRACT_ADDRESS`: The Ethereum address of the NFT collection you want to monitor
   - `YOUR_DISCORD_WEBHOOK_URL`: The webhook URL for your Discord channel

2. (Optional) Modify the `get_nft_marketplace` function to include more marketplace addresses if needed.

## Usage

Run the bot using the following command:

```
python nft_sales_bot.py
```

The bot will start monitoring for NFT sales and send notifications to your Discord channel when sales occur.

## Customization

- To monitor multiple NFT collections, you can create multiple instances of the script with different contract addresses.
- You can modify the Discord message format in the `send_discord_notification` function to suit your preferences.
- To add support for more marketplaces, update the `marketplaces` dictionary in the `get_nft_marketplace` function.

## Limitations

- This bot uses polling to check for new events. For high-volume collections, you might want to consider using WebSocket connections instead.
- The marketplace detection is basic and may not cover all NFT marketplaces.
- Error handling is minimal and should be expanded for production use.

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check [issues page](link-to-your-issues-page) if you want to contribute.

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Disclaimer

This bot is for educational purposes only. Make sure to comply with all relevant terms of service and legal requirements when using this bot.
