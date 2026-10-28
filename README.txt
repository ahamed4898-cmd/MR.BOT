SIGNAL BOT (free, runs on GitHub, sends signals to Telegram)

What it does: every ~15 minutes it reads live candles, runs your indicators (SMC, Liquidity BOS FVG OB,
BOS IDM OB) and sends new signals to your Telegram, with Entry, SL, TP1, TP2. It also tells you when TP1 is hit
(move SL to entry), and when the target or stop is hit. It never places orders: you place them yourself.

Files
  bot.js                      the bot
  indicators.js               the same indicator code as the website
  config.json                 which markets and indicators to watch (set "enabled": true/false)
  state.json                  the bot's memory (do not edit)
  .github/workflows/signals.yml   the 15-minute schedule

Secrets to add in GitHub (Settings > Secrets and variables > Actions):
  TELEGRAM_TOKEN     from @BotFather
  TELEGRAM_CHAT_ID   your chat id
  TWELVEDATA_KEY     only for forex and gold (free key from twelvedata.com)
