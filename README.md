# IBM Cloud - Watson Natural Language Understanding
A Node.js wrapper for the [Watson Natural Language Understanding](https://www.ibm.com/watson/developercloud/natural-language-understanding.html) service.

Description
-----------

The IBM Watson™ Natural Language Understanding service combines multiple NLP features to offer text analysis through natural language processing. The service offers text analysis through the following features:

*   [Concepts](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#concepts)
*   [Emotion](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#emotion)
*   [Entities](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#entities)
*   [Keywords](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#keywords)
*   [Metadata](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#metadata)
*   [Relations](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#relations)
*   [Semantic Roles](https://www.ibm.com/watson/developercloud/natural-language-understanding/api/v1/#semantic_roles)

Usage
-----

```js
var NaturalLanguageUnderstandingV1 = require('watson-developer-cloud/natural-language-understanding/v1.js');

var natural_language_understanding = new NaturalLanguageUnderstandingV1({
  'username': '{username}',
  'password': '{password}',
  'version_date': '2017-02-27'
});

var parameters = {
  'text': 'IBM is an American multinational technology company headquartered in Armonk, New York, United States, with operations in over 170 countries.',
  'features': {
    'entities': {
      'emotion': true,
      'sentiment': true,
      'limit': 2
    },
    'keywords': {
      'emotion': true,
      'sentiment': true,
      'limit': 2
    }
  }
}

natural_language_understanding.analyze(parameters, function(err, response) {
  if (err)
    console.log('error:', err);
  else
    console.log(JSON.stringify(response, null, 2));
});
```


#### IBM Cloud - Node.JS, Express, React.JS
Deployed on IBM Cloud: https://persistent-gerenuk-it.eu-gb.mybluemix.net/
