Discourse-SDK
=================================

## Installation
Using npm

`npm install --save discourse-sdk`

## Usage
In node.js 

```javascript
 var discourse = require('discourse-sdk');

 var client = new discourse('API-URL', 'API-KEY', 'USER-NAME');
 ```
### Categories

Gets a list of categories
```javascript
client.getCategories({},function(error, body, httpCode) {              
  console.log(body);                
});
```
Create new category
```javascript
client.createCategory('name', 'color', 'text_color', 'parent_category_id',function(error, body, httpCode) {              
  console.log(body);                
});
```
Get category Latest Topic
```javascript
client.getCategoryLatestTopic('category_slug', 'params',,function(error, body, httpCode) {              
  console.log(body);                
});
```
### Topics 

Create new Topic
```javascript
client.createTopic('title', 'raw', 'category' ,function(error, body, httpCode) {              
  console.log(body);                
});
```

Get Created Topics by given user

```javascript
client.getCreatedTopicsfunction('username' ,function(error, body, httpCode) {              
  console.log(body);                
});
```
Get Last Created Post Id

```javascript
client.getLastPostId(function(error, body, httpCode) {              
  console.log(body);                
});
```
Get Post by Id

```javascript
client.getPost('post-id',function(error, body, httpCode) {              
  console.log(body);                
});
```

### Users

Create New User

```javascript
client.createUser('name', 'email', 'username', 'password', 'active',function(error, body, httpCode) {              
  console.log(body);                
});
```
Delete User

```javascript
client.deleteUser('id','username', function(error, body, httpCode) {              
  console.log(body);                
});
```
Get User Details
```javascript
client.getUser('username', function(error, body, httpCode) {              
  console.log(body);                
});
```




## Credits
[discourse-api](https://github.com/dhyasama/discourse-api)
