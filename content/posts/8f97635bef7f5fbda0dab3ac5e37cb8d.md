---
aliases:
- https://github.com/obsei/obsei
title: 'GitHub - obsei/obsei: Obsei is a low code AI powered automation tool. It can
  be used in various business flows like social listening, AI based alerting, brand
  image analysis, comparative study and more .'
date: 2023-10-19
src_link: https://www.notion.so/obsei-obsei-Obsei-is-a-low-code-AI-powered-automation-tool-It-can-be-used-in-various-business-flow-33bacaae7baf41aa879435dd4c737775
src_date: '2023-10-19 08:52:00'
gold_link: https://github.com/obsei/obsei
gold_link_hash: 8f97635bef7f5fbda0dab3ac5e37cb8d
tags:
- '#host_github_com'
---


[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/obsei-flyer.png)](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/obsei-flyer.png)





---



[![](https://camo.githubusercontent.com/a4ad7df42a220a4baee42b40df3a3dd72b3ffabe7b16c11d78070f6f8f863a1f/68747470733a2f2f7374617469632e7769787374617469632e636f6d2f6d656469612f3539626334655f39373166313533663130376534386337393132623962326434636431623161347e6d76322e706e672f76312f66696c6c2f775f3137372c685f34392c616c5f632c715f38352c75736d5f302e36365f312e30305f302e30312c656e635f6175746f2f335f6564697465642e706e67)](https://www.oraika.com)




[![](https://github.com/obsei/obsei/workflows/CI/badge.svg?branch=master)](https://github.com/obsei/obsei/actions)
[![](https://camo.githubusercontent.com/23ba28eddd1192d4aad48468b610711af79f4e6e7bde8b151e60d19f7509a67a/68747470733a2f2f696d672e736869656c64732e696f2f707970692f6c2f6f62736569)](https://github.com/obsei/obsei/blob/master/LICENSE)
[![](https://camo.githubusercontent.com/9e8fe4ff5d421c6b9918bc74923b79d32e9a355e6de0aa312c6ecee6be26a98d/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f6f62736569)](https://pypi.org/project/obsei)
[![](https://camo.githubusercontent.com/58ed6a05f72366cd58538f82212321e8d60820c01c1c42a6d8c5a64e58ce3656/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f6f62736569)](https://pypi.org/project/obsei/)
[![](https://camo.githubusercontent.com/1ad30c8eb1dd00382b6786dd1e7651e93a3908996162139fb32d41b5aed34c16/68747470733a2f2f706570792e746563682f62616467652f6f627365692f6d6f6e7468)](https://pepy.tech/project/obsei)
[![](https://camo.githubusercontent.com/5762a687b24495afb299c2c0bc68674a2a7dfca9bda6ee444b9da7617d4223a6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f25463025394625413425393725323048756767696e67253230466163652d5370616365732d626c7565)](https://huggingface.co/spaces/obsei/obsei-demo)
[![](https://camo.githubusercontent.com/7bd07c3d388e6b917844baed1c45f5471a50cd27237aed8aa7c07768d0152aba/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c6173742d636f6d6d69742f6f627365692f6f62736569)](https://github.com/obsei/obsei/commits/master)
[![](https://camo.githubusercontent.com/8a9c1ee21407c5ec9b321bc50332d0c8c88af695b7dbca84c274caad5b1e6aff/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f6f627365692f6f627365693f7374796c653d736f6369616c)](https://github.com/obsei/obsei)
[![](https://camo.githubusercontent.com/623bf5101b25c947b68ad08666968fb3e883135e4c7a169f38d622fbfc00a39c/68747470733a2f2f696d672e736869656c64732e696f2f796f75747562652f6368616e6e656c2f73756273637269626572732f554371647667726f31427a553133746b416658336a434a413f7374796c653d736f6369616c)](https://www.youtube.com/channel/UCqdvgro1BzU13tkAfX3jCJA)
[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/logos/Slack_join.svg)](https://join.slack.com/t/obsei-community/shared_invite/zt-r0wnuz02-FAkAmhTAUoc6pD4SLB9Ikg)
[![](https://camo.githubusercontent.com/dd7bd9a39756f7c3780d497ae96054c3add56c4b4f010af87c8c78c5d78dd081/68747470733a2f2f696d672e736869656c64732e696f2f747769747465722f666f6c6c6f772f4f6273656941493f7374796c653d736f6369616c)](https://twitter.com/ObseiAI)





---


[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/gifs/obsei_flow.gif)](https://raw.githubusercontent.com/obsei/obsei-resources/master/gifs/obsei_flow.gif)




---



**Note**: Obsei is still in alpha stage hence carefully use it in Production. Also, as it is constantly undergoing development hence master branch may contain many breaking changes. Please use released version.



---


**Obsei** (pronounced "Ob see" | /əb-'sē/) is an open-source, low-code, AI powered automation tool. *Obsei* consists of -


* **Observer**: Collect unstructured data from various sources like tweets from Twitter, Subreddit comments on Reddit, page post's comments from Facebook, App Stores reviews, Google reviews, Amazon reviews, News, Website, etc.
* **Analyzer**: Analyze unstructured data collected with various AI tasks like classification, sentiment analysis, translation, PII, etc.
* **Informer**: Send analyzed data to various destinations like ticketing platforms, data storage, dataframe, etc so that the user can take further actions and perform analysis on the data.


All the Observers can store their state in databases (Sqlite, Postgres, MySQL, etc.), making Obsei suitable for scheduled jobs or serverless applications.


[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/Obsei_diagram.png)](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/Obsei_diagram.png)


### Future direction -


* Text, Image, Audio, Documents and Video oriented workflows
* Collect data from every possible private and public channels
* Add every possible workflow to an AI downstream application to automate manual cognitive workflows


Use cases
---------


*Obsei* use cases are following, but not limited to -


* Social listening: Listening about social media posts, comments, customer feedback, etc.
* Alerting/Notification: To get auto-alerts for events such as customer complaints, qualified sales leads, etc.
* Automatic customer issue creation based on customer complaints on Social Media, Email, etc.
* Automatic assignment of proper tags to tickets based content of customer complaint for example login issue, sign up issue, delivery issue, etc.
* Extraction of deeper insight from feedbacks on various platforms
* Market research
* Creation of dataset for various AI tasks
* Many more based on creativity 💡


Installation
------------


### Prerequisite


Install the following (if not present already) -


* Install [Python 3.7+](https://www.python.org/downloads/)
* Install [PIP](https://pip.pypa.io/en/stable/installing/)


### Install Obsei


You can install Obsei either via PIP or Conda based on your preference.
To install latest released version -



```
pip install obsei[all]
```

Install from master branch (if you want to try the latest features) -



```
git clone https://github.com/obsei/obsei.git
cd obsei
pip install --editable .[all]
```

Note: `all` option will install all the dependencies which might not be needed for your workflow, alternatively
following options are available to install minimal dependencies as per need -


* `pip install obsei[source]`: To install dependencies related to all observers
* `pip install obsei[sink]`: To install dependencies related to all informers
* `pip install obsei[analyzer]`: To install dependencies related to all analyzers, it will install pytorch as well
* `pip install obsei[twitter-api]`: To install dependencies related to Twitter observer
* `pip install obsei[google-play-scraper]`: To install dependencies related to Play Store review scrapper observer
* `pip install obsei[google-play-api]`: To install dependencies related to Google official play store review API based observer
* `pip install obsei[app-store-scraper]`: To install dependencies related to Apple App Store review scrapper observer
* `pip install obsei[reddit-scraper]`: To install dependencies related to Reddit post and comment scrapper observer
* `pip install obsei[reddit-api]`: To install dependencies related to Reddit official api based observer
* `pip install obsei[pandas]`: To install dependencies related to TSV/CSV/Pandas based observer and informer
* `pip install obsei[google-news-scraper]`: To install dependencies related to Google news scrapper observer
* `pip install obsei[facebook-api]`: To install dependencies related to Facebook official page post and comments api based observer
* `pip install obsei[atlassian-api]`: To install dependencies related to Jira official api based informer
* `pip install obsei[elasticsearch]`: To install dependencies related to elasticsearch informer
* `pip install obsei[slack-api]`:To install dependencies related to Slack official api based informer


You can also mix multiple dependencies together in single installation command. For example to install dependencies
Twitter observer, all analyzer, and Slack informer use following command -



```
pip install obsei[twitter-api, analyzer, slack-api]
```

How to use
----------


Expand the following steps and create a workflow -


**Step 1: Configure Source/Observer**


| **Twitter**  ---    ``` from obsei.source.twitter_source import TwitterCredentials, TwitterSource, TwitterSourceConfig  # initialize twitter source config source_config = TwitterSourceConfig(    keywords=["issue"], # Keywords, @user or #hashtags    lookup_period="1h", # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute)    cred_info=TwitterCredentials(        # Enter your twitter consumer key and secret. Get it from https://developer.twitter.com/en/apply-for-access        consumer_key="<twitter_consumer_key>",        consumer_secret="<twitter_consumer_secret>",        bearer_token='<ENTER BEARER TOKEN>',    ) )  # initialize tweets retriever source = TwitterSource() ``` |
| --- |
| **Youtube Scrapper**  ---    ``` from obsei.source.youtube_scrapper import YoutubeScrapperSource, YoutubeScrapperConfig  # initialize Youtube source config source_config = YoutubeScrapperConfig(     video_url="https://www.youtube.com/watch?v=uZfns0JIlFk", # Youtube video URL     fetch_replies=True, # Fetch replies to comments     max_comments=10, # Total number of comments and replies to fetch     lookup_period="1Y", # Lookup period from current time, format: `<number><d|h|m|M|Y>` (day|hour|minute|month|year) )  # initialize Youtube comments retriever source = YoutubeScrapperSource() ``` |
| **Facebook**  ---    ``` from obsei.source.facebook_source import FacebookCredentials, FacebookSource, FacebookSourceConfig  # initialize facebook source config source_config = FacebookSourceConfig(    page_id="110844591144719", # Facebook page id, for example this one for Obsei    lookup_period="1h", # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute)    cred_info=FacebookCredentials(        # Enter your facebook app_id, app_secret and long_term_token. Get it from https://developers.facebook.com/apps/        app_id="<facebook_app_id>",        app_secret="<facebook_app_secret>",        long_term_token="<facebook_long_term_token>",    ) )  # initialize facebook post comments retriever source = FacebookSource() ``` |
| **Email**  ---    ``` from obsei.source.email_source import EmailConfig, EmailCredInfo, EmailSource  # initialize email source config source_config = EmailConfig(    # List of IMAP servers for most commonly used email providers    # https://www.systoolsgroup.com/imap/    # Also, if you're using a Gmail account then make sure you allow less secure apps on your account -    # https://myaccount.google.com/lesssecureapps?pli=1    # Also enable IMAP access -    # https://mail.google.com/mail/u/0/#settings/fwdandpop    imap_server="imap.gmail.com", # Enter IMAP server    cred_info=EmailCredInfo(        # Enter your email account username and password        username="<email_username>",        password="<email_password>"    ),    lookup_period="1h" # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute) )  # initialize email retriever source = EmailSource() ``` |
| **Google Maps Reviews Scrapper**  ---    ``` from obsei.source.google_maps_reviews import OSGoogleMapsReviewsSource, OSGoogleMapsReviewsConfig  # initialize Outscrapper Maps review source config source_config = OSGoogleMapsReviewsConfig(    # Collect API key from https://outscraper.com/    api_key="<Enter Your API Key>",    # Enter Google Maps link or place id    # For example below is for the "Taj Mahal"    queries=["https://www.google.co.in/maps/place/Taj+Mahal/@27.1751496,78.0399535,17z/data=!4m5!3m4!1s0x39747121d702ff6d:0xdd2ae4803f767dde!8m2!3d27.1751448!4d78.0421422"],    number_of_reviews=10, )   # initialize Outscrapper Maps review retriever source = OSGoogleMapsReviewsSource() ``` |
| **AppStore Reviews Scrapper**  ---    ``` from obsei.source.appstore_scrapper import AppStoreScrapperConfig, AppStoreScrapperSource  # initialize app store source config source_config = AppStoreScrapperConfig(    # Need two parameters app_id and country.    # `app_id` can be found at the end of the url of app in app store.    # For example - https://apps.apple.com/us/app/xcode/id497799835    # `310633997` is the app_id for xcode and `us` is country.    countries=["us"],    app_id="310633997",    lookup_period="1h" # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute) )   # initialize app store reviews retriever source = AppStoreScrapperSource() ``` |
| **Play Store Reviews Scrapper**  ---    ``` from obsei.source.playstore_scrapper import PlayStoreScrapperConfig, PlayStoreScrapperSource  # initialize play store source config source_config = PlayStoreScrapperConfig(    # Need two parameters package_name and country.    # `package_name` can be found at the end of the url of app in play store.    # For example - https://play.google.com/store/apps/details?id=com.google.android.gm&hl=en&gl=US    # `com.google.android.gm` is the package_name for xcode and `us` is country.    countries=["us"],    package_name="com.google.android.gm",    lookup_period="1h" # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute) )  # initialize play store reviews retriever source = PlayStoreScrapperSource() ``` |
| **Reddit**  ---    ``` from obsei.source.reddit_source import RedditConfig, RedditSource, RedditCredInfo  # initialize reddit source config source_config = RedditConfig(    subreddits=["wallstreetbets"], # List of subreddits    # Reddit account username and password    # You can also enter reddit client_id and client_secret or refresh_token    # Create credential at https://www.reddit.com/prefs/apps    # Also refer https://praw.readthedocs.io/en/latest/getting_started/authentication.html    # Currently Password Flow, Read Only Mode and Saved Refresh Token Mode are supported    cred_info=RedditCredInfo(        username="<reddit_username>",        password="<reddit_password>"    ),    lookup_period="1h" # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute) )  # initialize reddit retriever source = RedditSource() ``` |
| **Reddit Scrapper**  ---   *Note: Reddit heavily rate limit scrappers, hence use it to fetch small data during long period*  ``` from obsei.source.reddit_scrapper import RedditScrapperConfig, RedditScrapperSource  # initialize reddit scrapper source config source_config = RedditScrapperConfig(    # Reddit subreddit, search etc rss url. For proper url refer following link -    # Refer https://www.reddit.com/r/pathogendavid/comments/tv8m9/pathogendavids_guide_to_rss_and_reddit/    url="https://www.reddit.com/r/wallstreetbets/comments/.rss?sort=new",    lookup_period="1h" # Lookup period from current time, format: `<number><d|h|m>` (day|hour|minute) )  # initialize reddit retriever source = RedditScrapperSource() ``` |
| **Google News**  ---    ``` from obsei.source.google_news_source import GoogleNewsConfig, GoogleNewsSource  # initialize Google News source config source_config = GoogleNewsConfig(    query='bitcoin',    max_results=5,    # To fetch full article text enable `fetch_article` flag    # By default google news gives title and highlight    fetch_article=True,    # proxy='http://127.0.0.1:8080' )  # initialize Google News retriever source = GoogleNewsSource() ``` |
| **Web Crawler**  ---    ``` from obsei.source.website_crawler_source import TrafilaturaCrawlerConfig, TrafilaturaCrawlerSource  # initialize website crawler source config source_config = TrafilaturaCrawlerConfig(    urls=['https://obsei.github.io/obsei/'] )  # initialize website text retriever source = TrafilaturaCrawlerSource() ``` |
| **Pandas DataFrame**  ---    ``` import pandas as pd from obsei.source.pandas_source import PandasSource, PandasSourceConfig  # Initialize your Pandas DataFrame from your sources like csv, excel, sql etc # In following example we are reading csv which have two columns title and text csv_file = "https://raw.githubusercontent.com/deepset-ai/haystack/master/tutorials/small_generator_dataset.csv" dataframe = pd.read_csv(csv_file)  # initialize pandas sink config sink_config = PandasSourceConfig(    dataframe=dataframe,    include_columns=["score"],    text_columns=["name", "degree"], )  # initialize pandas sink sink = PandasSource() ``` |



**Step 2: Configure Analyzer**
*Note: To run transformers in an offline mode, check [transformers offline mode](https://huggingface.co/transformers/installation.html#offline-mode).*


Some analyzer support GPU and to utilize pass **device** parameter.
List of possible values of **device** parameter (default value *auto*):


1. **auto**: GPU (cuda:0) will be used if available otherwise CPU will be used
2. **cpu**: CPU will be used
3. **cuda:{id}** - GPU will be used with provided CUDA device id




| **Text Classification**  ---   Text classification: Classify text into user provided categories.  ``` from obsei.analyzer.classification_analyzer import ClassificationAnalyzerConfig, ZeroShotClassificationAnalyzer  # initialize classification analyzer config # It can also detect sentiments if "positive" and "negative" labels are added. analyzer_config=ClassificationAnalyzerConfig(    labels=["service", "delay", "performance"], )  # initialize classification analyzer # For supported models refer https://huggingface.co/models?filter=zero-shot-classification text_analyzer = ZeroShotClassificationAnalyzer(    model_name_or_path="typeform/mobilebert-uncased-mnli",    device="auto" ) ``` |
| --- |
| **Sentiment Analyzer**  ---   Sentiment Analyzer: Detect the sentiment of the text. Text classification can also perform sentiment analysis but if you don't want to use heavy-duty NLP model then use less resource hungry dictionary based Vader Sentiment detector.  ``` from obsei.analyzer.sentiment_analyzer import VaderSentimentAnalyzer  # Vader does not need any configuration settings analyzer_config=None  # initialize vader sentiment analyzer text_analyzer = VaderSentimentAnalyzer() ``` |
| **NER Analyzer**  ---   NER (Named-Entity Recognition) Analyzer: Extract information and classify named entities mentioned in text into pre-defined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, etc  ``` from obsei.analyzer.ner_analyzer import NERAnalyzer  # NER analyzer does not need configuration settings analyzer_config=None  # initialize ner analyzer # For supported models refer https://huggingface.co/models?filter=token-classification text_analyzer = NERAnalyzer(    model_name_or_path="elastic/distilbert-base-cased-finetuned-conll03-english",    device = "auto" ) ``` |
| **Translator**  ---    ``` from obsei.analyzer.translation_analyzer import TranslationAnalyzer  # Translator does not need analyzer config analyzer_config = None  # initialize translator # For supported models refer https://huggingface.co/models?pipeline_tag=translation analyzer = TranslationAnalyzer(    model_name_or_path="Helsinki-NLP/opus-mt-hi-en",    device = "auto" ) ``` |
| **PII Anonymizer**  ---    ``` from obsei.analyzer.pii_analyzer import PresidioEngineConfig, PresidioModelConfig, \    PresidioPIIAnalyzer, PresidioPIIAnalyzerConfig  # initialize pii analyzer's config analyzer_config = PresidioPIIAnalyzerConfig(    # Whether to return only pii analysis or anonymize text    analyze_only=False,    # Whether to return detail information about anonymization decision    return_decision_process=True )  # initialize pii analyzer analyzer = PresidioPIIAnalyzer(    engine_config=PresidioEngineConfig(        # spacy and stanza nlp engines are supported        # For more info refer        # https://microsoft.github.io/presidio/analyzer/developing_recognizers/#utilize-spacy-or-stanza        nlp_engine_name="spacy",        # Update desired spacy model and language        models=[PresidioModelConfig(model_name="en_core_web_lg", lang_code="en")]    ) ) ``` |
| **Dummy Analyzer**  ---   Dummy Analyzer: Does nothing. Its simply used for transforming the input (TextPayload) to output (TextPayload) and adding the user supplied dummy data.  ``` from obsei.analyzer.dummy_analyzer import DummyAnalyzer, DummyAnalyzerConfig  # initialize dummy analyzer's configuration settings analyzer_config = DummyAnalyzerConfig()  # initialize dummy analyzer analyzer = DummyAnalyzer() ``` |



**Step 3: Configure Sink/Informer**


| **Slack**  ---    ``` from obsei.sink.slack_sink import SlackSink, SlackSinkConfig  # initialize slack sink config sink_config = SlackSinkConfig(    # Provide slack bot/app token    # For more detail refer https://slack.com/intl/en-de/help/articles/215770388-Create-and-regenerate-API-tokens    slack_token="<Slack_app_token>",    # To get channel id refer https://stackoverflow.com/questions/40940327/what-is-the-simplest-way-to-find-a-slack-team-id-and-a-channel-id    channel_id="C01LRS6CT9Q" )  # initialize slack sink sink = SlackSink() ``` |
| --- |
| **Zendesk**  ---    ``` from obsei.sink.zendesk_sink import ZendeskSink, ZendeskSinkConfig, ZendeskCredInfo  # initialize zendesk sink config sink_config = ZendeskSinkConfig(    # provide zendesk domain    domain="zendesk.com",    # provide subdomain if you have one    subdomain=None,    # Enter zendesk user details    cred_info=ZendeskCredInfo(        email="<zendesk_user_email>",        password="<zendesk_password>"    ) )  # initialize zendesk sink sink = ZendeskSink() ``` |
| **Jira**  ---    ``` from obsei.sink.jira_sink import JiraSink, JiraSinkConfig  # For testing purpose you can start jira server locally # Refer https://developer.atlassian.com/server/framework/atlassian-sdk/atlas-run-standalone/  # initialize Jira sink config sink_config = JiraSinkConfig(    url="http://localhost:2990/jira", # Jira server url     # Jira username & password for user who have permission to create issue    username="<username>",    password="<password>",    # Which type of issue to be created    # For more information refer https://support.atlassian.com/jira-cloud-administration/docs/what-are-issue-types/    issue_type={"name": "Task"},    # Under which project issue to be created    # For more information refer https://support.atlassian.com/jira-software-cloud/docs/what-is-a-jira-software-project/    project={"key": "CUS"}, )  # initialize Jira sink sink = JiraSink() ``` |
| **ElasticSearch**  ---    ``` from obsei.sink.elasticsearch_sink import ElasticSearchSink, ElasticSearchSinkConfig  # For testing purpose you can start Elasticsearch server locally via docker # `docker run -d --name elasticsearch -p 9200:9200 -e "discovery.type=single-node" elasticsearch:8.5.0`  # initialize Elasticsearch sink config sink_config = ElasticSearchSinkConfig(    # Elasticsearch server    hosts="http://localhost:9200",    # Index name, it will create if not exist    index_name="test", )  # initialize Elasticsearch sink sink = ElasticSearchSink() ``` |
| **Http**  ---    ``` from obsei.sink.http_sink import HttpSink, HttpSinkConfig  # For testing purpose you can create mock http server via postman # For more details refer https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/setting-up-mock/  # initialize http sink config (Currently only POST call is supported) sink_config = HttpSinkConfig(    # provide http server url    url="https://localhost:8080/api/path",    # Here you can add headers you would like to pass with request    headers={        "Content-type": "application/json"    } )  # To modify or converting the payload, create convertor class # Refer obsei.sink.dailyget_sink.PayloadConvertor for example  # initialize http sink sink = HttpSink() ``` |
| **Pandas DataFrame**  ---    ``` from pandas import DataFrame from obsei.sink.pandas_sink import PandasSink, PandasSinkConfig  # initialize pandas sink config sink_config = PandasSinkConfig(    dataframe=DataFrame() )  # initialize pandas sink sink = PandasSink() ``` |
| **Logger**  ---   This is useful for testing and dry running the pipeline.  ``` from obsei.sink.logger_sink import LoggerSink, LoggerSinkConfig import logging import sys  logger = logging.getLogger("Obsei") logging.basicConfig(stream=sys.stdout, level=logging.INFO)  # initialize logger sink config sink_config = LoggerSinkConfig(    logger=logger,    level=logging.INFO )  # initialize logger sink sink = LoggerSink() ``` |



**Step 4: Join and create workflow**
`source` will fetch data from the selected source, then feed it to the `analyzer` for processing, whose output we feed into a `sink` to get notified at that sink.



```
# Uncomment if you want logger
# import logging
# import sys
# logger = logging.getLogger(__name__)
# logging.basicConfig(stream=sys.stdout, level=logging.INFO)

# This will fetch information from configured source ie twitter, app store etc
source_response_list = source.lookup(source_config)

# Uncomment if you want to log source response
# for idx, source_response in enumerate(source_response_list):
#     logger.info(f"source_response#'{idx}'='{source_response.__dict__}'")

# This will execute analyzer (Sentiment, classification etc) on source data with provided analyzer_config
analyzer_response_list = text_analyzer.analyze_input(
    source_response_list=source_response_list,
    analyzer_config=analyzer_config
)

# Uncomment if you want to log analyzer response
# for idx, an_response in enumerate(analyzer_response_list):
#    logger.info(f"analyzer_response#'{idx}'='{an_response.__dict__}'")

# Analyzer output added to segmented_data
# Uncomment to log it
# for idx, an_response in enumerate(analyzer_response_list):
#    logger.info(f"analyzed_data#'{idx}'='{an_response.segmented_data.__dict__}'")

# This will send analyzed output to configure sink ie Slack, Zendesk etc
sink_response_list = sink.send_data(analyzer_response_list, sink_config)

# Uncomment if you want to log sink response
# for sink_response in sink_response_list:
#     if sink_response is not None:
#         logger.info(f"sink_response='{sink_response}'")
```


**Step 5: Execute workflow**
Copy the code snippets from **Steps 1 to 4** into a python file, for example `example.py` and execute the following command -

```
python example.py
```


Demo
----


We have a minimal [streamlit](https://streamlit.io/) based UI that you can use to test Obsei.


[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/obsei-ui-demo.png)](https://raw.githubusercontent.com/obsei/obsei-resources/master/images/obsei-ui-demo.png)


### Watch UI demo video


[![](https://camo.githubusercontent.com/1eccd6547a37b3262274c2cc0cfae97e22603a2762149cd75143c36f76d49cf0/68747470733a2f2f696d672e796f75747562652e636f6d2f76692f4754462d487939366776592f322e6a7067)](https://www.youtube.com/watch?v=GTF-Hy96gvY)


Check demo at [![](https://camo.githubusercontent.com/5762a687b24495afb299c2c0bc68674a2a7dfca9bda6ee444b9da7617d4223a6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f25463025394625413425393725323048756767696e67253230466163652d5370616365732d626c7565)](https://huggingface.co/spaces/obsei/obsei-demo)


(**Note**: Sometimes the Streamlit demo might not work due to rate limiting, use the docker image (locally) in such cases.)


To test locally, just run



```
docker run -d --name obesi-ui -p 8501:8501 obsei/obsei-ui-demo

# You can find the UI at http://localhost:8501

```

**To run Obsei workflow easily using GitHub Actions (no sign ups and cloud hosting required), refer to this [repo](https://github.com/obsei/demo-workflow-action)**.


Companies/Projects using Obsei
------------------------------


Here are some companies/projects (alphabetical order) using Obsei. To add your company/project to the list, please raise a PR or contact us via [email](/obsei/obsei/blob/master/contact@obsei.com).


* [Oraika](https://www.oraika.com): Contextually understand customer feedback
* [1Page](https://www.get1page.com/): Giving a better context in meetings and calls
* [Spacepulse](http://spacepulse.in/): The operating system for spaces
* [Superblog](https://superblog.ai/): A blazing fast alternative to WordPress and Medium
* [Zolve](https://zolve.com/): Creating a financial world beyond borders
* [Utilize](https://www.utilize.app/): No-code app builder for businesses with a deskless workforce


Articles
--------




| Sr. No. | Title | Author |
| --- | --- | --- |


Tutorials
---------




| Sr. No. | Workflow | Colab | Binder |
| --- | --- | --- | --- |
| 1 | Observe app reviews from Google play store, Analyze them by performing text classification and then Inform them on console via logger |
| PlayStore Reviews → Classification → Logger |  |  |
| 2 | Observe app reviews from Google play store, PreProcess text via various text cleaning functions, Analyze them by performing text classification, Inform them to Pandas DataFrame and store resultant CSV to Google Drive |
| PlayStore Reviews → PreProcessing → Classification → Pandas DataFrame → CSV in Google Drive |  |  |
| 3 | Observe app reviews from Apple app store, PreProcess text via various text cleaning function, Analyze them by performing text classification, Inform them to Pandas DataFrame and store resultant CSV to Google Drive |
| AppStore Reviews → PreProcessing → Classification → Pandas DataFrame → CSV in Google Drive |  |  |
| 4 | Observe news article from Google news, PreProcess text via various text cleaning function, Analyze them via performing text classification while splitting text in small chunks and later computing final inference using given formula |
| Google News → Text Cleaner → Text Splitter → Classification → Inference Aggregator |  |  |


**💡Tips: Handle large text classification via Obsei**
[![](https://raw.githubusercontent.com/obsei/obsei-resources/master/gifs/Long_Text_Classification.gif)](https://raw.githubusercontent.com/obsei/obsei-resources/master/gifs/Long_Text_Classification.gif)



Documentation
-------------


For detailed installation instructions, usages and examples, refer to our [documentation](https://obsei.github.io/obsei/).


Support and Release Matrix
--------------------------




| Linux | Mac | Windows | Remark |
| --- | --- | --- | --- |
| Tests | ✅ | ✅ | ✅ | Low Coverage as difficult to test 3rd party libs |
| PIP | ✅ | ✅ | ✅ | Fully Supported |
| Conda | ❌ | ❌ | ❌ | Not Supported |


Discussion forum
----------------


Discussion about *Obsei* can be done at [community forum](https://github.com/obsei/obsei/discussions)


Changelogs
----------


Refer [releases](https://github.com/obsei/obsei/releases) for changelogs


Security Issue
--------------


For any security issue please contact us via [email](mailto:contact@oraika.com)


Stargazers over time
--------------------


[![](https://camo.githubusercontent.com/6db074c29e0b6d0765ad470adea9aba18b8b5a4203b32df355bc6bd19eece982/68747470733a2f2f7374617263686172742e63632f6f627365692f6f627365692e737667)](https://starchart.cc/obsei/obsei)


Maintainers
-----------


This project is being maintained by [Oraika Technologies](https://www.oraika.com). [Lalit Pagaria](https://github.com/lalitpagaria) and [Girish Patel](https://github.com/GirishPatel) are maintainers of this project.


License
-------


* Copyright holder: [Oraika Technologies](https://www.oraika.com)
* Overall Apache 2.0 and you can read [License](https://github.com/obsei/obsei/blob/master/LICENSE) file.
* Multiple other secondary permissive or weak copyleft licenses (LGPL, MIT, BSD etc.) for third-party components refer [Attribution](https://github.com/obsei/obsei/blob/master/ATTRIBUTION.md).
* To make project more commercial friendly, we void third party components which have strong copyleft licenses (GPL, AGPL etc.) into the project.


Attribution
-----------


This could not have been possible without these [open source softwares](https://github.com/obsei/obsei/blob/master/ATTRIBUTION.md).


Contribution
------------


First off, thank you for even considering contributing to this package, every contribution big or small is greatly appreciated.
Please refer our [Contribution Guideline](https://github.com/obsei/obsei/blob/master/CONTRIBUTING.md) and [Code of Conduct](https://github.com/obsei/obsei/blob/master/CODE_OF_CONDUCT.md).


Thanks so much to all our contributors


[![](https://camo.githubusercontent.com/0167656c1ab70c40219b8d06c30bb6ced3b4d3adc2ba71251e7e037e836cbdb3/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d6f627365692f6f62736569)](https://github.com/obsei/obsei/graphs/contributors)