import asyncio
from aiogram import Bot, Dispatcher, types
from aiogram.filters import CommandStart

# Вставь сюда свой токен, который дал @BotFather (внутри кавычек!)
TOKEN = "8693038622:AAHkQTApX3ePlgnirOLhlzjy-AajyqXll6o"

# Создаем объекты бота и диспетчера
bot = Bot(token=TOKEN)
dp = Dispatcher()

# Этот кусок кода сработает, когда пользователь нажмет /start
@dp.message(CommandStart())
async def cmd_start(message: types.Message):
    await message.answer(f"Привет, {message.from_user.full_name}! Бот на Linux запущен. Чем займемся?")

# Этот кусок кода просто повторяет любое написанное сообщение (Эхо)
@dp.message()
async def echo(message: types.Message):
    await message.answer(f"Ты написал: {message.text}")

# Главная функция, которая запускает бота в работу
async def main():
    print("Бот успешно запущен и слушает сообщения...")
    await dp.start_polling(bot)

if __name__ == "__main__":
    try:
        asyncio.run(main())
    except KeyboardInterrupt:
        print("Бот выключен")
