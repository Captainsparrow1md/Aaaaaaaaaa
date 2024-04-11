from telegram import Bot, Update
from telegram.ext import CommandHandler, Updater

# Define your bot token
TOKEN = "6963966651:AAGlnNuQdVMLNMcM1GNxBdqE_N7DPJERG0M"

def start(update, context):
    context.bot.send_message(chat_id=update.effective_chat.id, text="Hello! I'm your bot.")

def echo(update, context):
    context.bot.send_message(chat_id=update.effective_chat.id, text=update.message.text)

def main():
    # Create the bot object
    bot = Bot(token=TOKEN)

    # Get the dispatcher to register handlers
    updater = Updater(bot=bot, use_context=True)
    dp = updater.dispatcher

    # Register command handlers
    dp.add_handler(CommandHandler("start", start))
    dp.add_handler(CommandHandler("echo", echo))

    # Start the Bot
    updater.start_polling()

    # Run the bot until you press Ctrl-C or the process receives SIGINT,
    # SIGTERM or SIGABRT
    updater.idle()

if __name__ == '__main__':
    main()
