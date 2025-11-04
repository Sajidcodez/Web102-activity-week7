# CryptoCurrency 💰

A modern cryptocurrency browser application built with React that allows users to explore and search through the top 50 cryptocurrencies by trading volume in real-time.

## Features

- **Live Cryptocurrency Data**: Fetches real-time data on the top 50 cryptocurrencies by total top tier volume
- **Search Functionality**: Search through cryptocurrencies by name, symbol, algorithm, or proof type
- **Responsive UI**: Dark-themed interface with a fixed sidebar navigation
- **Coin Information Display**: View detailed information about each cryptocurrency including:
  - Coin image/icon
  - Full name
  - Symbol (ticker)
  - Algorithm & Proof Type
- **Filtered Results**: Automatically filters out cryptocurrencies with incomplete data (N/A values)

## Tech Stack

- **Frontend**: React 18
- **Build Tool**: Vite
- **Styling**: CSS
- **API**: CryptoCompare API (https://cryptocompare.com)
- **Package Manager**: npm

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm

### Installation

1. Clone the repository
```bash
git clone https://github.com/Sajidcodez/Web102-activity-week7.git
cd Web102-activity-week7
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
```bash
# Copy the example file
cp .env.example .env

# Add your CryptoCompare API key to .env
VITE_APP_API_KEY=your_api_key_here
```

Get your free API key from [CryptoCompare](https://www.cryptocompare.com/cryptopian/api)

### Running the App

**Development Mode:**
```bash
npm run dev
```
The app will start at `http://localhost:5173`

**Build for Production:**
```bash
npm run build
```

**Preview Production Build:**
```bash
npm run preview
```

## Project Structure

```
src/
├── App.jsx          # Main app component with API fetching logic
├── App.css          # Main styling
├── main.jsx         # React entry point
├── index.css        # Global styles
└── Components/
    ├── CoinInfo.jsx # Individual coin display component
    └── SideNav.jsx  # Sidebar navigation component
```

## How It Works

1. **Data Fetching**: On app load, `App.jsx` makes a request to CryptoCompare's API to fetch the top 50 cryptocurrencies
2. **State Management**: Stores the fetched data in React state
3. **Search/Filter**: Users can search through the coins, which filters results in real-time
4. **Display**: The filtered coins are mapped through the `CoinInfo` component to display each cryptocurrency

## Security

- API keys are stored in a `.env` file and are never exposed in the source code
- The `.env` file is ignored by git to prevent accidental exposure
- Use `.env.example` as a template for setting up environment variables

## License

This Activity is part of the Web102 curriculum
