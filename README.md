# price

Bitcoin's USD price per block (`height_to_ohlc.json`) and per day (`date_to_ohlc.json`), as open, high, low,
close in dollars.

- Through block 941,899 (2026-03-23): the price snapshot from Bitview v0.1.9.
- From block 941,900: Binance's BTCUSDT one-minute candles, built per block as v0.1.9's fetcher built them: a
  block's open is the close of its previous block's minute, its high and low are over the minutes after it through
  its own (timestamps floored to the minute), its close its own minute's. Days are Binance's daily candles;
  `dateindex` 0 is the genesis day, 2009-01-03, and 1 is 2009-01-09, a day each after.

Bitview's oracle is scored against it: see brk_oracle's README in the Bitview repository.
