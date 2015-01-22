# s15_Hao_data_lecture_notes
*Task of this course: write a server in Jason, write a client in Jason*

Data life cycle:
Question -> collection -> clean up -> storage -> processing analysis -> query + visalize + act

Question -> curation (prioritisation), triage, persistance

*Jan,15,2015*
===========
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


*Jan,22,2015*
============
Git: 
=====
* git branch: review the branches in the directory
* git branch branch_name: create a new branch
* git checkout commit: move the current state of your copy to a commit
* git commit-m "Commit Message"
* git merge branch_name: merges the named branch into the *current* branch
* git pull [remote_repository] [branch_name]
* git push [remote_repository]: push all the updted branches to their equivalent in the remote repository
* log: gives a history of commits
* remote: setup remote knowledge of remote respositories
* diff: check differences between current commit and other commit
* fetch: similiar to pull, get the changes but do not integrate
* reset: move to the current head
* mv: move a files location within a repository
* rebase: rebase the branch, change master
* branches are pointers.
* conflicts: <<<<< conflicts ==== >>>>>> you have to fix the conflicts
 
Github:
=======
* workflow: master -> branch -> pull request -> master
* Github like branching more than rebasing: accurate history
* git commit -m "fix bug ...": should write clear commit
* open pull request: send pull request, to ask master to merge (tip: use "@mention")
* fork: github specific, a fork is an exact copy of a repository, use it to run experiments without screwing things up, do not need authorization (difference from clone??)
* branch: you must have collaborator access
* discuss and review code
* merge and deploy
 
Contacts:
========
rackup -p 4000 ***.rb

NODE_ENV ?

rspec --color test_client.rb

type "node" in terminal will enter javascript environment (node is a wapper arount javascript)

server side: sinatra to develop web-application


