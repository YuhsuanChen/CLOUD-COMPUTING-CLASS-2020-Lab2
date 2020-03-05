# Lab2 Answer

## Task 2.1.1: Word Count 1
###### Q211:
```
[('the', 1343), (',', 1251), ('.', 810), (')', 638), ('(', 637), 
('of', 586), ('to', 491), ('a', 470), (':', 454), ('in', 417)]
Total words count: 25169
```

## Task 2.1.2: Remove punctuation
###### Q212:
```
[('the', 1444), ('of', 586), ('to', 531), ('in', 506), ('a', 481), 
('and', 346), ('is', 289), ('we', 279), ('that', 275), ('this', 268)]
Total words count: 19593
```

## Task 2.1.3: Stop Words
###### Q213a Why "Tensorflow" is not the most frequent word? Which are the Stop Words?
Because there're some words appear frequently is necessary for making sentence but not that important such as following stop words. 
```
Stop word:['i', 'me', 'my', 'myself', 'we', 'our', 'ours', 'ourselves', 'you', "you're",
"you've", "you'll", "you'd", 'your', 'yours', 'yourself', 'yourselves', 'he', 'him',
'his', 'himself', 'she', "she's", 'her', 'hers', 'herself', 'it', "it's", 'its', 'itself', 
'they', 'them', 'their', 'theirs', 'themselves', 'what', 'which', 'who', 'whom', 'this', 
'that', "that'll", 'these', 'those', 'am', 'is', 'are', 'was', 'were', 'be', 'been', 'being', 
'have', 'has', 'had', 'having', 'do', 'does', 'did', 'doing', 'a', 'an', 'the', 'and', 'but', 
'if', 'or', 'because', 'as', 'until', 'while', 'of', 'at', 'by', 'for', 'with', 'about', 
'against', 'between', 'into', 'through', 'during', 'before', 'after', 'above', 'below', 
'to', 'from', 'up', 'down', 'in', 'out', 'on', 'off', 'over', 'under', 'again', 'further', 
'then', 'once', 'here', 'there', 'when', 'where', 'why', 'how', 'all', 'any', 'both', 'each', 
'few', 'more', 'most', 'other', 'some', 'such', 'no', 'nor', 'not', 'only', 'own', 'same', 
'so', 'than', 'too', 'very', 's', 't', 'can', 'will', 'just', 'don', "don't", 'should', 
"should've", 'now', 'd', 'll', 'm', 'o', 're', 've', 'y', 'ain', 'aren', "aren't", 'couldn', 
"couldn't", 'didn', "didn't", 'doesn', "doesn't", 'hadn', "hadn't", 'hasn', "hasn't",
'haven', "haven't", 'isn', "isn't", 'ma', 'mightn', "mightn't", 'mustn', "mustn't", 'needn', 
"needn't", 'shan', "shan't", 'shouldn', "shouldn't", 'wasn', "wasn't", 'weren', 
"weren't", 'won', "won't", 'wouldn', "wouldn't"]
```
###### Q213b Output after remove stopwords: 
```
[('tensorflow', 193), ('data', 102), ('tensor', 99), ('code', 90), ('learning', 81), 
('function', 74), ('one', 73), ('use', 65), ('example', 64), ('available', 63)]
Total words count: 2998
```

## Task 2.2.1: Accessing your twitter account information
###### Q221 Is the data printed correctly? Is it yours? 

Yes
```
Name: Alice Chen
Location: Barcelona
Followers: 0
Created: 2020-02-27 18:57:08
Description: Account for CC
```

## Task 2.2.2: Accessing Tweets
###### Q22: Keep track of your executions.

**Case1 Show one tweet:**

After execute 

`for status in tweepy.Cursor(api.home_timeline).items(1):
	print(status.text)`
Output: 

```Hola! First post on Friday```

**Case2 Status of the tweet:** 

After execute 

`for status in tweepy.Cursor(api.home_timeline).items(1):
   	print(json.dumps(status._json, indent=2))`
	
Output: 

```
{
  "created_at": "Fri Feb 28 08:12:31 +0000 2020",
  "id": 1233303954769006593,
  "id_str": "1233303954769006593",
  "text": "Second Tweet nice weather",
  "truncated": false,
  "entities": {
    "hashtags": [],
    "symbols": [],
    "user_mentions": [],
    "urls": []
  },
  "source": "<a href=\"https://mobile.twitter.com\" rel=\"nofollow\">Twitter Web App</a>",
  "in_reply_to_status_id": null,
  "in_reply_to_status_id_str": null,
  "in_reply_to_user_id": null,
  "in_reply_to_user_id_str": null,
  "in_reply_to_screen_name": null,
  "user": {
    "id": 1233103719463575552,
    "id_str": "1233103719463575552",
    "name": "Alice Chen",
    "screen_name": "AliceCh81581517",
    "location": "Barcelona",
    "description": "Account for CC",
    "url": null,
    "entities": {
      "description": {
        "urls": []
      }
    },
    "protected": false,
    "followers_count": 0,
    "friends_count": 0,
    "listed_count": 0,
    "created_at": "Thu Feb 27 18:57:08 +0000 2020",
    "favourites_count": 0,
    "utc_offset": null,
    "time_zone": null,
    "geo_enabled": false,
    "verified": false,
    "statuses_count": 2,
    "lang": null,
    "contributors_enabled": false,
    "is_translator": false,
    "is_translation_enabled": false,
    "profile_background_color": "F5F8FA",
    "profile_background_image_url": null,
    "profile_background_image_url_https": null,
    "profile_background_tile": false,
    "profile_image_url": "http://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_image_url_https": "https://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_link_color": "1DA1F2",
    "profile_sidebar_border_color": "C0DEED",
    "profile_sidebar_fill_color": "DDEEF6",
    "profile_text_color": "333333",
    "profile_use_background_image": true,
    "has_extended_profile": false,
    "default_profile": true,
    "default_profile_image": true,
    "following": false,
    "follow_request_sent": false,
    "notifications": false,
    "translator_type": "none"
  },
  "geo": null,
  "coordinates": null,
  "place": null,
  "contributors": null,
  "is_quote_status": false,
  "retweet_count": 0,
  "favorite_count": 0,
  "favorited": false,
  "retweeted": false,
  "lang": "en"
}{
  "created_at": "Fri Feb 28 08:12:31 +0000 2020",
  "id": 1233303954769006593,
  "id_str": "1233303954769006593",
  "text": "Second Tweet nice weather",
  "truncated": false,
  "entities": {
    "hashtags": [],
    "symbols": [],
    "user_mentions": [],
    "urls": []
  },
  "source": "<a href=\"https://mobile.twitter.com\" rel=\"nofollow\">Twitter Web App</a>",
  "in_reply_to_status_id": null,
  "in_reply_to_status_id_str": null,
  "in_reply_to_user_id": null,
  "in_reply_to_user_id_str": null,
  "in_reply_to_screen_name": null,
  "user": {
    "id": 1233103719463575552,
    "id_str": "1233103719463575552",
    "name": "Alice Chen",
    "screen_name": "AliceCh81581517",
    "location": "Barcelona",
    "description": "Account for CC",
    "url": null,
    "entities": {
      "description": {
        "urls": []
      }
    },
    "protected": false,
    "followers_count": 0,
    "friends_count": 0,
    "listed_count": 0,
    "created_at": "Thu Feb 27 18:57:08 +0000 2020",
    "favourites_count": 0,
    "utc_offset": null,
    "time_zone": null,
    "geo_enabled": false,
    "verified": false,
    "statuses_count": 2,
    "lang": null,
    "contributors_enabled": false,
    "is_translator": false,
    "is_translation_enabled": false,
    "profile_background_color": "F5F8FA",
    "profile_background_image_url": null,
    "profile_background_image_url_https": null,
    "profile_background_tile": false,
    "profile_image_url": "http://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_image_url_https": "https://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_link_color": "1DA1F2",
    "profile_sidebar_border_color": "C0DEED",
    "profile_sidebar_fill_color": "DDEEF6",
    "profile_text_color": "333333",
    "profile_use_background_image": true,
    "has_extended_profile": false,
    "default_profile": true,
    "default_profile_image": true,
    "following": false,
    "follow_request_sent": false,
    "notifications": false,
    "translator_type": "none"
  },
  "geo": null,
  "coordinates": null,
  "place": null,
  "contributors": null,
  "is_quote_status": false,
  "retweet_count": 0,
  "favorite_count": 0,
  "favorited": false,
  "retweeted": false,
  "lang": "en"
}
```

**Case3 Check followers:**

After execute 

`for follower in tweepy.Cursor(api.friends).items(1):
  	print(json.dumps(follower._json, indent=2))`
	
Output: --Nothing-- as is a new account there's no follower

**Case4 Show some tweets:**

After execute 

`for tweet in tweepy.Cursor(api.user_timeline).items(1):
	print(json.dumps(tweet._json, indent=2))`
	
Output:

```
{
  "created_at": "Fri Feb 28 08:12:31 +0000 2020",
  "id": 1233303954769006593,
  "id_str": "1233303954769006593",
  "text": "Second Tweet nice weather",
  "truncated": false,
  "entities": {
    "hashtags": [],
    "symbols": [],
    "user_mentions": [],
    "urls": []
  },
  "source": "<a href=\"https://mobile.twitter.com\" rel=\"nofollow\">Twitter Web App</a>",
  "in_reply_to_status_id": null,
  "in_reply_to_status_id_str": null,
  "in_reply_to_user_id": null,
  "in_reply_to_user_id_str": null,
  "in_reply_to_screen_name": null,
  "user": {
    "id": 1233103719463575552,
    "id_str": "1233103719463575552",
    "name": "Alice Chen",
    "screen_name": "AliceCh81581517",
    "location": "Barcelona",
    "description": "Account for CC",
    "url": null,
    "entities": {
      "description": {
        "urls": []
      }
    },
    "protected": false,
    "followers_count": 0,
    "friends_count": 0,
    "listed_count": 0,
    "created_at": "Thu Feb 27 18:57:08 +0000 2020",
    "favourites_count": 0,
    "utc_offset": null,
    "time_zone": null,
    "geo_enabled": false,
    "verified": false,
    "statuses_count": 2,
    "lang": null,
    "contributors_enabled": false,
    "is_translator": false,
    "is_translation_enabled": false,
    "profile_background_color": "F5F8FA",
    "profile_background_image_url": null,
    "profile_background_image_url_https": null,
    "profile_background_tile": false,
    "profile_image_url": "http://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_image_url_https": "https://abs.twimg.com/sticky/default_profile_images/default_profile_normal.png",
    "profile_link_color": "1DA1F2",
    "profile_sidebar_border_color": "C0DEED",
    "profile_sidebar_fill_color": "DDEEF6",
    "profile_text_color": "333333",
    "profile_use_background_image": true,
    "has_extended_profile": false,
    "default_profile": true,
    "default_profile_image": true,
    "following": false,
    "follow_request_sent": false,
    "notifications": false,
    "translator_type": "none"
  },
  "geo": null,
  "coordinates": null,
  "place": null,
  "contributors": null,
  "is_quote_status": false,
  "retweet_count": 0,
  "favorite_count": 0,
  "favorited": false,
  "retweeted": false,
  "lang": "en"
}
```
## Task 2.3: Tweet pre-processing: 
###### Q23 
With pre-processing:

`['RT', '@JordiTorresBCN', ':', 'just', 'an', 'example', '!', ':D', 'http://JordiTorres.Barcelona', '#masterMEI']`

Without pre-processing:

`['RT', '@', 'JordiTorresBCN', ':', 'just', 'an', 'example', '!', ':', 'D', 'http', ':', '//JordiTorres.Barcelona', '#', 'masterMEI']`

The preprocessing result keep @-mentions, emoticons, URLs, and #hash-tags

## Q24: How long have you been working on this session? What have been the main difficulties you have faced and how have you solved them? 
Around 3 hours

When I was doing Task 2.1 I have problem when using this line: nltk.download('punkt') and always get error msg, then I solved problem by downloading the pkg from http://www.nltk.org/nltk_data/ and put it into our project and it works. (Yuhsuan Chen)

No special difficulties I have faced but it took some times to understand how to use these interface and functions. (Yi-Chiau Li)
