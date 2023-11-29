- API to (Login /logout)
- API to (add,edit,delete,getAll) for categories
- API to (add,edit,delete) product to category
- API to get all products by categoryId
- API to search by name for product / by categoryId & name for product
  --> design patterns and services I've used:-
  1- repoository pattern: it has made my code organised and clean by have queries inside repositories instead of controllers
  and it reduces queries duplications and it makes a layer for the code that deals with database seperated from
  the layer that deals with the business logic .. it also makes controller dependancy of entity framework to another
  layer so, if the organization has decided to change EF to dapper or change database provider to such as (sql)
  to another on such as (postgresql).
  you can find it with interfaces in (interfaces) folder and job class that implements interfaces in (repository) folder.

      2- unit of work: it gather all my transactions of CRUD operations in a single transaction .. you find it in (Iunit of work , unit of work) fils.

      3-Dependency Injection: I've injected repositories to unit of work so i can access classes -thats are accessed itself from repositories-
      	from unit of work.

      3- dto: it enables me to pass data with multiple attributes in one shot from client to server and vice-versa .. and you cand find it in (Dtos) folder.

      4- auto mapper: it maps different objects attributes so it takes out of my hands how to map those different objects .. you find it
      	in (MappingProfile) file inside (helpers) folder.
