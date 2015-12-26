# Programming-assigment-2
## Put comments here that give an overall description of what your
## functions do

#### Makecahematrix function creates an special object matrix and calculates the inverse 
## of this matrix;storing it in the cache memory, making it available for a further call.

makeCacheMatrix <- function(x = matrix()) {
  inv <- NULL
  set <- function(y) {
    x <<- y
    inv <<- NULL
  }
  get <- function() x
  setinverse<- function(solve) inv<<-solve
  getinverse <- function() inv
  list(set = set, get = get,
       setinverse = setinverse,
       getinverse = getinverse)
}

makeCacheMatrix(x)


cacheSolve <- function(x, ...){
  inv <-x$getreverse()
  if (!is.null(inv)) {
    message("getting cached matrix")
    return(inv)
  } else {
    inv<-x$get()
    inv<-solve(data)
    x$setreverse(inv)
    return(inv)
    solve (inv)
    inv
  }
  
  cacheSolve(x)
  
        ## Return a matrix that is the inverse of 'x'
