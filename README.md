# Photo Viewer

An applicationn to view a gallery of photos.

## Libaries being used:

nodemon - For convenience of server testing/channges
express - For better API building
cors - for CORS across browsers

csvtojson - Converting csv to json formatting

node-cache - Caching module that works like memcached (lightweight 55kb)
  vs memory-cache (not as popular and was not updated as frequently)

React - create-react-app 
  vs setting up webpack which can take awhile

react-thunk
  vs react-saga for pure functions and better side effects handling
  react-saga is better for large scale and this is an SPA handling small routing async

Redux - to dispatch store for asynchronous calls with react-thunk and dispatching props to components

## How to start up project

### Production

Build the server first on one terminal:
```npm run server```

Build the react components on another terminal:
```npm run build```

### Development

Build the server using on one terminal:
```npm run nodemon```

Build the react components on another terminal:
```npm start```

Notes: server runs locally port 3001, on build react integrates with it and development are separate (react on 3000, server on 3001)

## Walkthrough

Generally you would have a home page and then a user or some verification to see images/feed (i.e. instagram)

Currently the homepage just renders all the images using React/Redux

From homepage -> user logins -> gets verified -> redirects to /images

Things missing:

Front End:

  I. Filtering dimension drop down
  
  II. Infinite scrolling passed on backend pagination fetch/re-render component
  
  III. Toggle grayscale checkbox

  Bugs:
    I. Query params needed to be fixed, hardcoded token as a temp 

## React Component Structure

1. Components

  1a. App
  
  1b. Photo Gallery


## Picture dimensions query from server

I. ?width= && length=

Various sizes:
1. 300x200
2. 100x100
3. 250x250
4. 400x200
5. 300x300


II. ?page= && limit=

III. ?token=

## Test Screenshots

### Fetching cache retrieval 

![Test Image 1](/test_SS/1.png)

Cache retrieval on sucess

![Test Image 1](/test_SS/1b.png)

### fetching images based on query params

![Test Image 2](/test_SS/2.png)

Using cache to filter for query params true

![Test Image 2](/test_SS/2b.png)


### Token testing

With token 

![Test Image 3](/test_SS/3a.png)

Without Tokem

![Test Image 3](/test_SS/3b.png)


### Grayscale testing
![Test Image 4](/test_SS/4.png)


### Production testing
![Test Image 5](/test_SS/5.png)
