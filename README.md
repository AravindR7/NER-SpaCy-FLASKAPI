# NER-SpaCy-FLASK
 Our goal is to build an API that we provide text, for example, a News  article (or any article) as input, our named entity extractor will then identify and extract four types of entities: organization, person, location and money.


[!https://cdn-images-1.medium.com/max/800/1*F85X-bnJRqTaXVMyTdoUwA.png]

To build the API, we will need to create two files:

1. index.html to handle the template of the API.
2. app.py to handle the requests and return the output file.

app.py

Our app.py file is simple and easy to understand. It contains the main code that will be executed by the python interpreter to run flask web application, it includes the spacy code for recognising the named entities.
- We ran our app as a single module; thus we initialised the new flask instance with the __name__ to let flask know know that it can find the HTML template folder(templates) in the same directory where it is located.
- we use the route decorator(@app.route('/')) to specify that url should trigger the execution of the index function.
- Our index function simply renders the index.html file, which is located in the template folder
- Inside the process function we apply NLP to the raw text user will enter, and extract predetermined named entities(Organization, Person, Geopolitical & Money) from the raw text.
- We use the POST method to transport the form data to the server in message body. Finally by setting the debug=True arguement inside the app.run method, we further activaed Flask's debugger.
- We use the run function to run the application on the server when this script is directly executed by the Python interpreter, which we ensured  using the o=if statement with __name__ == '__main__'.
