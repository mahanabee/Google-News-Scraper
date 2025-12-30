## Google News API のセットアップ
以下の手順に従って、[Google News API](https://brightdata.jp/products/serp-api/google-search/news) をセットアップしてください。  
1. **Bright Data アカウントにログインします。** **Web Scraper API** タブに移動します。  
2. 検索バーに **Google News** と入力し、選択します:

   <img width="650" alt="google-news-scraper-screenshot-bright-data-web-scraper-api" src="https://github.com/user-attachments/assets/53da065a-4975-4821-9ba8-9912c9da939f">

3. **Start setting an API call** をクリックして、API の設定を開始します:

   <img width="650" alt="google-news-scraper-screenshot-start-setting-api-call" src="https://github.com/user-attachments/assets/a608922c-5f2f-46f9-b687-ed62c4eeaf97">

4. **Get API Token** を選択して、一意の API token を生成します:

   <img width="650" alt="google-news-scraper-screenshot-get-api-token" src="https://github.com/user-attachments/assets/4e7f6044-dd26-43eb-b354-0726c87e83ce">

5. **Add token** をクリックして、新しい token を作成します:

   <img width="650" alt="google-news-scraper-screenshot-add-token" src="https://github.com/user-attachments/assets/f83863c7-2174-478a-9698-ed0b23e7c962">

6. API token を安全に保存します。API コールを行う際に必要になります:

   <img width="650" alt="google-news-scraper-screenshot-new-api-token" src="https://github.com/user-attachments/assets/11d79010-94fb-41a3-9c38-3baea71aa240">

7. **Dataset ID** を見つけるには、**Management APIs** タブに移動します

   <img width="650" alt="google-news-scraper-screenshot-dataset-id" src="https://github.com/user-attachments/assets/d13b7901-1c66-4a13-b3f8-71b5b2bb42ad">

8. **Data Collection APIs** タブで、**Add inputs** を使用して複数の inputs を設定します:

     <img width="650" alt="google-news-scraper-screenshot-trigger-data-collection-api" src="https://github.com/user-attachments/assets/6005a9a8-430b-448e-82f2-17c390b15155">

9. パラメータを調整すると、右側に CURL コマンドが生成されます。次のことができます:
   - このコマンドを使用して、[Trigger Data Collection API](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/trigger-a-collection) を直接実行します
   - これらのパラメータを、[code](https://github.com/luminati-io/Google-News-Scraper?tab=readme-ov-file#ready-to-use-python-code) 内の `_trigger_collection` 関数に [渡します](https://github.com/luminati-io/Google-News-Scraper?tab=readme-ov-file#key-input-parameters)