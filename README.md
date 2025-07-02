# technical_analyzer
Technical Analysis Module

This module provides a complete solution for performing technical analysis on OHLCV (Open, High, Low, Close, Volume) cryptocurrency data. It is designed to work as part of an AI trading assistant system, enabling the extraction of key technical indicators and structured signal summaries from raw market data.

Features

Data Cleaning: Handles missing data and supports different timestamp formats.

Indicator Calculation: Computes a wide range of technical indicators across trend, momentum, volatility, and volume categories, using the pandas-ta library.

Crossover Detection: Detects Golden Cross and Death Cross patterns.

Rule-Based Sentiment Scoring: Assigns a simple numerical score based on combined indicator logic to represent technical sentiment.

Structured Summary Generation: Outputs a dictionary summary of key indicators and signals, useful for decision-making or model input.


Indicator Categories

Trend Indicators: Simple and exponential moving averages (SMA/EMA), MACD, ADX, Aroon, and Parabolic SAR.

Momentum Indicators: RSI, Stochastic Oscillator, CCI, Momentum, and Rate of Change.

Volatility Indicators: Bollinger Bands, ATR, Keltner Channels, and Donchian Channels.

Volume Indicators: On-Balance Volume (OBV), Chaikin Money Flow (CMF), Money Flow Index (MFI), and VWAP.


Usage

To use this module, initialize the TechnicalAnalyzer class with a cleaned OHLCV DataFrame. The generate_all_indicators() method will compute the full set of indicators and append them to the DataFrame. You can then call get_structured_summary() to extract a simplified dictionary summary.

Integration

This module is intended to be used within a larger trading assistant framework. It optionally integrates with a MarketDataFetcher module for live data and a custom logger utility. If not available, it defaults to basic Python logging.

Development and Testing

The module includes a __main__ block that allows you to run it standalone for testing. This requires a market data fetching module located at src/data/market_data.py. The testing block fetches real-time OHLCV data, runs indicator calculations, and prints the output summary.

Requirements

Python 3.8 or higher

pandas

pandas-ta

numpy


File Location and Dependencies

The module is located at cryptsignal/technical_analysis.py. It may depend on:

src/data/market_data.py for live data

utils/logger.py for logging


License

This module is released under the MIT License and can be freely used, modified, and distributed with proper attribution.

Author

Developed as part of a full-stack AI trading assistant project by Chukwujiekwu Collins Ifedi 
