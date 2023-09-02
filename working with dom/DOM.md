## DOM

browser exposes web APi to allow javascript to work with parsed document

- dom is strictly tied to browsers

## Document and Window

- document is root DOM node and has access to element querying,DOM content
- window is the active browser Window/Tab.It acts as a global storage for script and also provides access to window specific properties and methods

> console.dir(document)
> console.dir(window) - browser api , document is part of window Object

- dom is tree like structure, where element nodes (div,h1) and text nodes(text we write)

## querying Elements

- querySelector(),getElementById() - returns single elements -(by css selector , by ID respectively)

* querySelectorAll(),getElementByTagName() , getElementsByClassName() - returns collection /array of elements - (by css selectors, tag name ,class name)
* querySelectorAll() returns snapshot , so if we add or remove elements , it does not return new data

* getElementByTagName() , getElementsByClassName() returns live , so updating will return updated dom
