# go-training

A practical go training lab by [at15][at15]

## Syllabus

It has three parts, language basic, utility tasks and real word project

### Language basic

Following are some common questions that you should be able to answer

- control flow
  - how to break nested for loop?
  - if you have a very long `if else if else if else` what can you use instead?
  - if you take address of the temp var using `&v` in `for v := range mySlice`, what will happen?
- slice, map
  - initialization, nil value, you can use nil slice but not nil map, why?
  - concurrency, do you always need lock for concurrent access on slice?
- struct
  - difference between value and pointer receiver
  - struct method vs function with a struct in parameters
  - struct embedding, is it inheritance?
  - field tags, where do you need them, are they used at compile time or runtime?
- interface
  - how to find all the structs that implement a interface, IDE & cli
  - how to implement a interface
  - check if a struct implement certain interface in one line
- function
  - function as parameter
  - closure
  - anonymous function
  - function that implements an interface (hint: check `net/http`)
- package
  - does `github.com/at15/abc` includes `github.com/at15/abc/def`
  - import other projects
  - `$GOPATH` and vendor (glide, dep)
  - go mod
- goroutine
  - wait multiple go routine to finish
  - quit all goroutines if one of them failed
  - limited concurrency
  - concurrency vs parallelism? (hint: google the video from Rob Pike)
- test
  - how to test a http server in unit test
  - how to test your http api server logic without start a real http server
  - table test
  - golden file pattern

### Utility tasks

Following are some common small tasks that you should be able to write using standard library and just looking at godoc

- create dir if it not exists
- list all folder and files under a directory recursively
  - generate a pretty output like the `tree` command
  - allow specify level
- ssh into a server without using `ssh` command, there is a `crypto/ssh` package
  - stream output to current terminal
  - get the output directly
  - ssh into multiple servers in parallel
- a simple http server
  - serve static content
  - render template using `html/template`

### Real word projects

Just some rough ideas

LeetCode Scraper

- run a server and craw periodically
- design a schema to save multiple users activity in database
  - first in memory implementation
  - MySQL using raw SQL statement
    - how to prevent SQL injection?
  - ORM
- provide a JSON API
  - with swagger doc (just to learn swagger)
- spin up cluster using terraform
- deploy using container manually on GCP
- deploy using Kubernetes on GCP using GKE

Restaurant picker

- save restaurant
- save historical events, i.e. went to xxx, A like xxx, B don't like xxx, C didn't eat anything (`/w\`)
- random pick one based on people attending

[at15]: http://github.com/at15