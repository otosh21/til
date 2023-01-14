### コードからの利用  
1. OpenAIにサインアップ／ログインしてAPIキーを取得する  
    1. 右上のアカウントアイコンをクリック  
    2. View API keys を選択  
    3. Create new secret keyボタンをクリック  
    4. APIキーをコピー（一度しか表示されないため、忘れずにコピーしておくこと）  
2. PyPIからopenaiモジュールをインストールする  
    1. シェル、コマンドプロンプト、Visual Studio Codeの開発環境のシェル等から　pip install openai　コマンドを実行  
3. openai.Completion.createクラスメソッドを呼び出す  
    1. api_key属性にAPIキーを設定  
    2. openai.Completion.createクラスメソッドを呼び出す  
  
```  
KEY = 'APIキー'  
  
import openai  
  
openai.api_key = KEY  
  
response = openai.Completion.create(  
  model = 'text-davinci-003',
  prompt = '晴れた日曜日の午後には何をすればいいかな？',  
  temperature = 0.7,  
  max_tokens = 256,  
  top_p = 1,  
  frequency_penalty = 0,  
  presence_penalty = 0  
)  

print(responce['choices'][0]['text'])  
```  
