# nodepay-airdrop-bot

A bot for automating Nodepay airdrop interactions, including session management and pinging with flexible connection options (proxy or direct).

## Requirements

1. **Node.js** (version 14 or higher)
2. **npm** (Node package manager)

## Installation

To get started with the Nodepay Airdrop Bot:

1. Clone the repository:

    ```bash
    git clone https://github.com/dante4rt/nodepay-airdrop-bot.git
    cd nodepay-airdrop-bot
    ```

2. Install the dependencies:

    ```bash
    npm install
    ```

## Configuration

Before running the bot, you need to set up your configuration:

### 1. `token.txt` (Required)

To get your Bearer token:

1. **Register for a Nodepay account**:
   - Go to [Nodepay Registration Page](https://app.nodepay.ai/register?ref=QQ51zuerWUH82iS) and sign up for an account.

2. **Get your token**:
   - Open **DevTools** in your browser (right-click > Inspect or press `Ctrl+Shift+I`).
   - Go to the **Console** tab in DevTools.
   - Type the following command so that you can find your token:

     ```javascript
     allow pasting
     ```
        - Then type the following command to get your token:
     ```javascript
     localStorage.getItem('np_webapp_token')
     ```

   - This will return the Bearer token. **Copy the token** (without the `Bearer` prefix, just the alphanumeric string).

3. **Paste the token in `token.txt`**:
   - Create a `token.txt` file in the root of your project and paste your token in the file (one token per line).

     ```javascript
     nano token.txt
     ```
     Then press Ctrl + X => Y => Enter
     
Example `token.txt`:

```text
ey...
ey...
ey...
```

### 2. `proxy.txt` (Optional)

Only required if you choose to use proxies when running the bot.

- Add your proxy details in `proxy.txt`. Each line should have the format:

  ```text
  host:port:username:password
  ```

- Example:

  ```text
  123.45.67.89:8080:username:password
  123.45.67.89:8080:username:password
  123.45.67.89:8080:username:password
  ```

## Running the Bot

To start the bot, run the following command:

```bash
screen -S nodepaybot
```

Then

```bash
npm start
```

When you start the bot, you'll be prompted to:

1. Choose whether to use proxies or direct connection
2. Select between single or multiple account mode

### Connection Modes

1. **Proxy Mode**
   - Requires valid `proxy.txt` file
   - Uses different IP addresses for connections
   - Better for running multiple accounts
   - More anonymous operation

2. **Direct Mode**
   - No proxy configuration needed
   - Uses your device's IP address
   - Simpler setup
   - Good for single account usage

Then press Ctl + A + D to detach from screen

## Logs

The bot will log all activity, including:

- Connection status for each session (UID)
- Ping status for each session
- Connection type (proxy/direct) used
- IP address information (when using proxies)

Logs are stored in `bot.log` and can also be seen in the console.

## Donations

If you would like to support the development of this project, you can make a donation using the following addresses:

- **Solana**: `EBbY1GskRSgwJcN3cuUCaZqk5zzpsr7A6ku7yg4TCGJa`
- **EVM**: `0x895b2c93976f72E6dB0Bf88265a74f34733abd3D`
- **BTC**: `tb1qfw8zztm67fjzgtru05udwtzq8f069fv8l7am2t`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
