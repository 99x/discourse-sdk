Discourse-SDK
=================================

## Installation
Using npm

`npm install --save discourse-sdk`

## Usage
In node.js 

`var discourse = require('discourse-sdk');`

`var client = new discourse('API-URL', 'API-KEY', 'USER-NAME');`

Gets a list of categories
```javascript
client.getCategories({},function(error, body, httpCode) {              
  console.log(body);                
});
```
Create new category
```javascript
client.createCategory(name, color, text_color, parent_category_id,function(error, body, httpCode) {              
  console.log(body);                
});
```
Get category Latest Topic
```javascript
client.getCategoryLatestTopic(category_slug, params,,function(error, body, httpCode) {              
  console.log(body);                
});
```
