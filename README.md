import discord # インストールした discord.py

client = discord.Client() # 接続に使用するオブジェクト


# 起動時に通知してくれる処理
@client.event
async def on_ready():
    print('Kento botがログインしました')


# 「！こんにちは」と発言したら「こんにちは。天気はどう？？」が返る処理
@client.event
async def on_message(message):
    if message.content.startswith('！こんにちは'):
        reply = 'こんにちは。天気はどう？？'
        await client.send_message(message.channel, reply)


   # botの接続と起動
#（tokenにはbotアカウントのアクセストークンを入れてください）
client.run('NDkxNTM3ODUyNjIzMDkzNzYw.DvOgMg.gDYDTvtUSsO0dgtJctIZsX795vU')
