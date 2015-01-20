# 15_Hao_data_lecture_notes
*Task of this course: write a server in Jason, write a client in Jason*

Data life cycle:
Question -> collection -> clean up -> storage -> processing analysis -> query + visalize + act

Question -> curation (prioritisation), triage, persistance

*Jan,15,2015*
Markdown:
========
Two types of Markdown:

1. Standard markdown
2. Github flavor markdown

What can be done with Markdown?
* Styling
* Word formatting
* Add images
* Create links
* Code blocks
 
Services:
=========
Get, post, delete, put
Web browser -> Web server -> handeler

.html: local file on disk


RESTful: representation, state, transfer (for REST)
=========
An architecture, serves based system to separate resource and resprentation language

URI(general class of URL, URL is a kind of URI) -> Resources

CRUD: create, read, update, destroy

Web of a REST architecture. 

For any users (URI, refer to some resources), we could apply html to it (i.e. get, post, put, delete)
* Get: read, get back current state of resource (git: {id})
* Post: create a new user (git: {data})
* Put: update an existing history (git: update the {id})
* Delete: destroy

Query string: /search?a1=r1 + a2=r2 (limit: 1024 characters) 

Example:
========
get 'api/1.0/whattimeisit'

   "hellow word"
   
end
   
curl http://localhost:3000/api/1.0/whattimeisit (typed in terminal to compile)

get 'api/1.0/whattimeisit' do

   {status: true, message: "hello world"}.to_json + "\n" (hash table)
   
   {status: true, messge: Time.now}.to_json + "\n"
   
end

Questions:
* What's the database?
* id?
* What are the input, output (format client expecting)?
* How to deal with errors?

Jan,20,2015
=============
REST
====
Post - create; Get - read; Put - update; Delete - delete (CRUD)

POST and PUT methods typically send data, also in JSON format, maybe in URL or in the body of the HTTP request

ISSUES:
======
* Security: how do you authenticate users?
* Identity: how are ids assigned to resources?
* Failure: how do we handle failure situations?
         JSON, HTTP Status Codes (404,500,etc.), combination of both
* Persistence: how are resources stored? (Java stores things in memory; Ruby stores things in file)

Example Contacts Web service, Technology used:
* Sinatra
* Rspec: testing
* Typhoeus: Ruby library to do http request
* Node: about Javascript
* Express: on server side, handeling requests

Display -> Hadoop, Hive -> NoSQL

rspect --color test_client.rb



