# Google News Scraper

[![Promo](https://github.com/bright-jp/Google-News-Scraper/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.jp/products/serp-api/google-search/news?promo=github15) 

このリポジトリでは、Google News からニュースデータを収集するための 2 つの方法を提供します。
- **無料の方法:** 小規模プロジェクトや学習に最適です
- **Google News API:** 大規模で信頼性が高く、リアルタイムのデータ抽出に最適です

## Table of Contents

- [Method 1: Free Google News Scraper](#method-1-free-google-news-scraper)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Output](#output)
- [Common Scraping Challenges](#common-scraping-challenges)
- [Method 2: Bright Data Google News API](#method-2-bright-data-google-news-api)
  - [Key Benefits](#key-benefits)
  - [Getting Started with the Google News API](#getting-started-with-the-google-news-api)
  - [Key Input Parameters](#key-input-parameters)
  - [Sample Result](#sample-result)
  - [Ready-to-Use Python Code](#ready-to-use-python-code)
  - [Understanding the API Implementation](#understanding-the-api-implementation)
  - [Customizing Your Data Collection](#customizing-your-data-collection)

## Method 1: Free Google News Scraper
<img width="700" alt="image" src="https://github.com/user-attachments/assets/a7d34ffe-17c6-4c59-acbf-aaf84ed1b13e">

この無料ツールを使用すると、興味のある任意のトピックに基づいてニュース記事を収集できます。見出しから公開日まで、すべてがきれいに整理された形で取得できます。

### Prerequisites
- Python 3.9+
- 主要パッケージ 2 つ:
  - [aiohttp](https://pypi.org/project/aiohttp/)（リクエスト送信用）
  - [beautifulsoup4](https://pypi.org/project/beautifulsoup4/)（HTML 解析用）

### Installation
1. リポジトリをクローンします:

    ```bash
    git clone https://github.com/bright-jp/Google-News-Scraper.git
    ```
3. プロジェクトディレクトリに移動します:

    ```bash
    cd Google-News-Scraper
    ```
4. 必要な依存関係をインストールします:

    ```bash
    pip install -r requirements.txt
    ```
### Usage
1. `free_scraper` ディレクトリに移動し、`main.py` を開きます
2. ファイル内で検索語を定義します:

    ```bash
    search_terms = [
        "artificial intelligence",
        "climate change",
        "space exploration",
        # Add more search terms as needed
    ]
    ```
3. スクレイパーを実行します:

    ```bash
    python main.py
    ```
### Output
スクレイパーは JSON ファイルを生成します:
- 検索語ごとの個別 JSON ファイル
- すべての検索語のデータを含む `combined_results.json` ファイル

JSON 出力内の各記事には次が含まれます:
```json
{
    "title": "OpenAI launches full o1 model with image uploads and analysis, debuts ChatGPT Pro - VentureBeat",
    "link": "https://news.google.com/rss/articles/CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR?oc=5",
    "publication_date": "Thu, 05 Dec 2024 18:00:00 GMT",
    "source": "VentureBeat",
    "source_url": "https://venturebeat.com",
    "guid": "CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR",
}
```

👉 完全な出力例は、[free_scraper/data/](https://github.com/bright-jp/Google-News-Scraper/tree/main/free_scraper/data) ディレクトリで確認できます。

## Common Scraping Challenges
Google News からのスクレイピングはかなり難しい場合があります。よくある問題は次のとおりです:
1. **CAPTCHA とアンチボットの仕組み:** Google はボットがコンテンツにアクセスするのを防ぐため、CAPTCHA やレート制限の仕組みを頻繁に採用しています。
2. **スケーラビリティ:** 大量データのスクレイピングや高頻度のスクレイピングは、無料スクレイパーでは負荷が大きすぎる場合があります。
3. **グローバルおよびローカライズされたニュースへのアクセス:** 地域や言語が異なるスクレイパーをカスタマイズするには、多くの場合かなりの労力と手動調整が必要です。

## Method 2: Bright Data Google News API
より堅牢な仕組みが必要ですか？ [Bright Data の Google News API](https://brightdata.jp/products/serp-api/google-search/news) についてご紹介します。検討する価値がある理由は次のとおりです:

### Key Benefits
- **インフラの悩みはゼロ:** プロキシや CAPTCHA のことは忘れてください
- **スケール前提:** 高トラフィックを優れたパフォーマンスで処理します
- **グローバル対応:** どの国・どの言語のニュースも取得できます
- **プライバシー優先:** GDPR および CCPA に準拠
- **成功課金:** 成功したリクエストに対してのみ課金されます
- **購入前に試せます:** テスト用に API を 20 回無料で呼び出せます

## Getting Started with the Google News API
> Google News API のセットアップに関する詳細ガイドは、[Step-by-Step Setup Guide](https://github.com/bright-jp/Google-News-Scraper/blob/main/google_news_api_setup.md) をご覧ください。
### Key Input Parameters
| **Parameter**| **Required?** | **Description**                                            | **Example**               |
|---------------|--------------|------------------------------------------------------------|---------------------------|
| `url`         | Yes          | ベースとなる Google News URL                                   | `news.google.com`|
| `keyword`     | Yes          | 検索トピック                        | `"ChatGPT"`             |
| `country`     | No           | ニュースの取得元の国                                | `"US"`                    |
| `language`    | No           | 希望する言語                                | `"en"`                    |

### Sample Result
API は次のような結果を返します:
```json
{
    "url": "https://www.tomsguide.com/news/live/12-days-of-openai-live-blog-chatgpt-sora",
    "title": "12 Days of OpenAI Day 2 LIVE: o1 full is here and every new ChatGPT AI announcement as it happens",
    "publisher": "Tom's Guide",
    "date": "2024-12-06T20:54:01.000Z",
    "category": null,
    "keyword": "chatgpt",
    "country": "US",
    "image": "https://news.google.com/api/attachments/CC8iK0NnNW9SbTFVTWtkNGFGSjJSVGhGVFJDb0FSaXNBaWdCTWdhQmtJcWpOQWM=-w200-h112-p-df-rw",
    "timestamp": "2024-12-08T10:06:05.122Z",
    "input": {
        "url": "https://news.google.com/",
        "keyword": "chatgpt",
        "country": "US",
        "language": "en",
    },
}
```
👉 完全な出力例は、[news_scraper_output.json](https://github.com/bright-jp/Google-News-Scraper/blob/main/google-news-api-scraper/data/news_scraper_output.json) ファイルで確認できます。

### Ready-to-Use Python Code
開始用のスクリプトはこちらです:
```python
import requests
import json
import time


class BrightDataNews:
    def __init__(self, api_token):
        self.api_token = api_token
        self.headers = {
            "Authorization": f"Bearer {api_token}",
            "Content-Type": "application/json",
        }
        self.dataset_id = "gd_lnsxoxzi1omrwnka5r"

    def collect_news(self, search_queries):
        """
        Collect Google News articles using BrightData API
        """
        # 1. Trigger data collection
        print("Starting news collection...")
        trigger_response = self._trigger_collection(search_queries)
        snapshot_id = trigger_response.get("snapshot_id")
        print(f"Snapshot ID: {snapshot_id}")

        # 2. Wait for data to be ready
        print("Waiting for data...")
        while True:
            status = self._check_status(snapshot_id)
            print(f"Status: {status}")

            if status == "ready":
                # Check if data is actually available
                data = self._get_data(snapshot_id)
                if data and len(data) > 0:
                    break
            time.sleep(10)  # Wait 10 seconds before next check
        # 3. Get and save the data
        print("Saving data...")
        filename = f"news_scraper_output.json"
        with open(filename, "w", encoding="utf-8") as f:
            json.dump(data, f, indent=2, ensure_ascii=False)
        print(f"✓ Data saved to {filename}")
        print(f"✓ Collected {len(data)} news articles")
        return data

    def _trigger_collection(self, search_queries):
        """Trigger news data collection"""
        response = requests.post(
            "https://api.brightdata.com/datasets/v3/trigger",
            headers=self.headers,
            params={"dataset_id": self.dataset_id, "include_errors": "true"},
            json=search_queries,
        )
        return response.json()

    def _check_status(self, snapshot_id):
        """Check collection status"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/progress/{snapshot_id}",
            headers=self.headers,
        )
        return response.json().get("status")

    def _get_data(self, snapshot_id):
        """Get collected data"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/snapshot/{snapshot_id}",
            headers=self.headers,
            params={"format": "json"},
        )
        return response.json()
```
使用方法はこちらです:
```python
# Initialize the client
news_client = BrightDataNews("<YOUR_API_TOKEN>")

# Define what you want to collect
queries = [
    {
        "url": "https://news.google.com/",
        "keyword": "artificial intelligence startups",
        "country": "US",
        "language": "en",
    },
    {
        "url": "https://news.google.com/",
        "keyword": "tech industry layoffs",
        "country": "US",
        "language": "en",
    },
]

# Start collection
try:
    news_data = news_client.collect_news(queries)
    print(f"Successfully collected {len(news_data)} articles")
except Exception as e:
    print(f"Collection failed: {str(e)}")
```
### Understanding the API Implementation
1. **API トークンの設定**
    - まず最初に、API トークンが必要です
    - まだお持ちでない場合は、[setup guide](https://github.com/bright-jp/Google-News-Scraper/blob/main/google_news_api_setup.md) をご確認ください
2. **収集の開始**
    - 検索パラメータを API に渡します
    - `snapshot_id` が返ってきます
3. **進捗のモニタリング**
    - 処理には数分かかります
    - このコードではステータスを自動的に確認します:
      - "running" = データ収集中
      - "ready" = 結果を取得するタイミングです！
4. **データの取得**
    - ステータスが "ready" になったら、結果を取得して保存します
    - データは整った JSON 形式で提供されます
    - 各記事には、先ほど説明したすべてのフィールドが含まれます

## Customizing Your Data Collection
次のパラメータを使用して、結果を微調整できます:
| **Parameter**       | **Type**   | **Description**                                            | **Example**                  |
|---------------------|------------|------------------------------------------------------------|------------------------------|
| `limit`             | `integer`  | 入力あたりの最大結果数                                   | `limit=10`                   |
| `include_errors`    | `boolean`  | トラブルシューティング用にエラーレポートを取得します                     | `include_errors=true`        |
| `notify`            | `url`      | 完了時に通知を受け取るための Webhook 通知 URL  | `notify=https://notify-me.com/` |
| `format`            | `enum`     | 出力形式（例: JSON, NDJSON, JSONL, CSV）         | `format=json`                |

💡 **Pro Tip:** データを [external storage](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-deliver-to-external-storage) に配信するか、[webhook](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-webhook) に配信するかも選択できます。

----

さらに詳細が必要な場合は、[official API docs](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview) をご確認ください。