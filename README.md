# [hap.py](https://hap-py.herokuapp.com/)
Too lazy to find some funny jokes? hap.py is here to help! hap.py is a one stop facial recognition software that will send you the greatest (and most appropriate) jokes based on your mood and age. On top of that, jokes will be sent straight to your phone, allowing you to be connected with the top jokes at your convenience. 

![Index](https://github.com/happy-peddiehacks/hap.py/blob/master/static/assets/img/Screenshots/index.png)
![Results](https://github.com/happy-peddiehacks/hap.py/blob/master/static/assets/img/Screenshots/results.png)

## Inspiration
Whenever we feel happy, sad, angry, or anything in between, jokes can provide the necessary moral support to make your day one thousand times better. But how could we make jokes *even better*? Ever since we have been stuck at home, finding shortcuts to every day problems has been essential. That's where facial recognition can come in! Having a mood-detecting software that **also** sends you jokes would be the perfect combination to satisfy your everyday needs.

## What it does
This application utilises the [Microsoft Face API](https://azure.microsoft.com/en-us/services/cognitive-services/face/) in conjunction with the [Twilio API](http://twilio.com/) and [Joke API](https://rapidapi.com/Sv443/api/jokeapi-v2?endpoint=apiendpoint_e5399e8c-6633-4c02-8063-42e2dd17e9fe) to text you a number of jokes based on your mood. There are more jokes the less happy you are deemed to be. 

## How we built it
1. Create routes to index.html and results.html with Flask
2. Use [Microsoft Face API](https://azure.microsoft.com/en-us/services/cognitive-services/face/) to detect age and emotion (happiness index)
3. Calculates joke category based on emotion detected
4. Parses through [Joke API](https://rapidapi.com/Sv443/api/jokeapi-v2?endpoint=apiendpoint_e5399e8c-6633-4c02-8063-42e2dd17e9fe) and retrieves joke with corresponding parameters
5. Send joke to inputted phone number with [Twilio API](http://twilio.com/)
6. Run localhost and test out the app!

## Challenges we ran into
- Used an outdated version of [Joke API](https://rapidapi.com/Sv443/api/jokeapi-v2?endpoint=apiendpoint_e5399e8c-6633-4c02-8063-42e2dd17e9fe) at first
- Version control issues with Git
- Converting web data to JSON objects
- Developing algorithm to relate happiness and joke category

## Accomplishments that we're proud of
- Utilized multiple APIs in conunction with each other
- Developed fully functional web application using Flask
- Learned how to create full stack apps

## What we learned
We learned how to work with multiple APIS at the same time and how to create a full stack web app. We also learned and developed an algorith to relate happiness and jokes as well as the basics of Flask webpage development.  

## What's next for hap.py
Now that we've developed the basic framework for hap.py, we have a lot in store for the future! First, we plan on cleaning up the UI/UX of the web app to provide a more aesthetic interface for users. Once that is done, we will deploy hap.py to the internet using Heroku, so that it will be accessible to everyone!

## Installation
1. Download the code
2. Create a `.env` file in the home directory
3. Put the following in the `.env` file, and replace items in brackets with your own information
```
FACE_KEY={YOUR_FACE_KEY}
TWILIO_SID={YOUR_TWILIO_SID}
TWILIO_KEY={YOUR_TWILIO_KEY}
TWILIO_NUMBER={YOUR_TWILIO_NUMBER}
JOKES_API={JOKES_API}
```
4. Run the code with `flask run` and view it in the browser!

## Website
Click [here](https://hap-py.herokuapp.com/) to try the app yourself!
