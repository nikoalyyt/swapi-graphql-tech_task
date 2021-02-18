# swapi-graphql-tech_task

I used https://graphql.org/swapi-graphql to create the GraphQl queries

To get the url for the Graphql queries requests through postman I sent a GET request to https://graphql.org/swapi-graphql and copied the graphql endpoint from the response which is https://swapi-graphql.netlify.app/.netlify/functions/index

In order to run GraphQL queries through postman I put them into the Body of the requests using the GraphQL radio button there which allows you to put such queries.

Explanation on how the queries work:

#1. All species in A New Hope
First through a request I found that the filmID of "A New Hope" is 1, so I used it as an argument for the film object. Then I added "title" to be gotten as part of the film field. SpeciesConnection is used as a connection between film and psecies and as a part of it I get the species' names field.

#2. Person which is Droid
First through some request I found out that the Droid species id is c3BlY2llczoy so I ussed it as an filtering argument in the species object. From species I request only the name of the species in order "Droid" to be returned in the reponse to give more visibility. Then I use personConnection field so I can get name, birth date, homeworld and eyecolor for the Droid person.

#3 Count of all people in A New Hope
Once again using the id of the film "A New Hope" as an argument for the film object I request the "characterConnection" field which contains information for the totalCount of people in the movie and has a child field "characters" which contains info for people's id, name and gender.

#4 Person with unique id = 4
Here I pass the personID=4 as an argument for the person object. Below as child fields of person I request the name, birthYear, eyeColor, homeworld (and its name as a child field) and I use the "starshipConnection" field in order to get the person's starship's name as its child field.


P.S: Responses from request are also saved in the Postman Collection.
