# hubot-memegen

A hubot script to create funny memes based on your own image templates

## setup

First create in your hubot location a directory to put there your meme template images and it's definition. You can also use the examples directory content included in this project as base.

    $ mkdir memegen
    $ cp examples/* ./memegen

There create a templates definition file in json format. You can find an example of this file in the examples directory

Then you'll need to set two environment variables. The first one is the apikey of the service [imagebin.ca](http://imagebin.ca)

    HUBOT_MEMEGEN_IMAGE_BIN_APIKEY=<apikey>
    HUBOT_MEMEGEN_TEMPLATES_FILE=memegen/templates.json


You'll need to add this as a dependency to your hubot:

    $ npm install --save hubot-memegen

Lastly add it to the list of external dependencies in `external-scripts.json`:

    ["hubot-memegen"]

## Current commands

    - memegen <template id> <phrase> - Create a meme using the requested template and phrase

## Example
    - hubot memegen dog Shuch Hubot!
