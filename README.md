# Newman Reporter HTML And HTML-Extra Using Json-Server And Postman For macOS

## Technology and Tool Used
- Postman
- Node Js
- newman
- Json-Server
- npm
- Visual Studio Code

## Prerequisites

- You must have installed node js to your system
- Postman
- NPM
- Newman
- Json-Server

## Scenario of this project

- The user can create a user
- The user can create a user by id,name
- The user can get all users
- The user can get individual user by user id
- The user can update a user by user id
- The user can delete a user by user id

## API Documents

https://documenter.getpostman.com/view/16548351/2s946feCjX 

## ## How to run this project

- clone this project
- open this project in visual studio code

## npm install

            sudo npm install
            
- check the npm version

          npm -v
  
## Newman Install

         sudo npm install -g newman
  
- check the newman version

        newman -v
  
## Install json-Server

       sudo npm install -g json-server
      
- check the version

      json-server -v
  
- start the json-server

      json-server --watch user.json
  
- Export collection in the same directory

## Install newman-reporter-html

        $ sudo npm install -g newman-reporter-html


## Usage

          $ newman run https://www.getpostman.com/collections/631643-f695cab7-6878-eb55-7943-ad88e1ccfd65-JsLv -r html

## Options

- With Newman CLI

  ![image](https://github.com/Mamun104/newman-reporter-html-and-htmlextra-using-jsonserver-and-postman/assets/78067017/5b896873-3156-497b-98cf-c42e1141aa95)

- Custom templates (currently handlebars only) can be passed to the HTML reporter via --reporter-html-template <path> with --reporters html and --reporter-html-export. The default template is used in all other cases.

## With Newman as a Library

  - The CLI functionality is available for programmatic use as well.

      const newman = require('newman');

newman.run({
    collection: require('./examples/sample-collection.json'), // can also provide a URL or path to a local JSON file.
    reporters: 'html',
    reporter: {
        html: {
            export: './htmlResults.html', // If not specified, the file will be written to `newman/` in the current working directory.
            template: './customTemplate.hbs' // optional, this will be picked up relative to the directory that Newman runs in.
        }
    }
}, function (err) {
	if (err) { throw err; }
    console.log('collection run complete!');
});


## Compatibility

![image](https://github.com/Mamun104/newman-reporter-html-and-htmlextra-using-jsonserver-and-postman/assets/78067017/cab2b3a2-f4a5-4f3e-b8be-58a61d8271a6)


## Install newman-reporter-html-extra

- A Newman HTML reporter that has been extended to include the separation of the iteration runs so these are no longer aggregated together and also some additional handlebars helpers to enable users to create better custom templates.

- This reporter comes with a dashboard style summary landing page and a set of different tabs which contain the detailed request information. There are also a few optional configuration flags available, to tailor the final report in a number of different ways.

- To globally install the htmlextra package:


        sudo npm install -g newman-reporter-htmlextra

  ## Usage

  - In order to enable this reporter, specify htmlextra in Newman's -r or --reporters option. The following command will create a new report in the ./newman directory, if the directory does not exist, it will be created as part of the Newman run.

       sudo newman run collection.json -r htmlextra

## Report Example

![image](https://github.com/Mamun104/newman-reporter-html-and-htmlextra-using-jsonserver-and-postman/assets/78067017/a9d91f3d-8fe1-46c2-aad5-0a241279b6d2)

# Newman-Reporter-HTML-Result:

![image](https://github.com/Mamun104/newman-reporter-html-and-htmlextra-using-jsonserver-and-postman/assets/78067017/f6369cc9-63c5-48ec-8211-77dfdfac0bc9)

# Newman-Reporter-HTML-Extra-Result:


![image](https://github.com/Mamun104/newman-reporter-html-and-htmlextra-using-jsonserver-and-postman/assets/78067017/a9d91f3d-8fe1-46c2-aad5-0a241279b6d2)
