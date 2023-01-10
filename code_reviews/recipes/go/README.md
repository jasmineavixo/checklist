# Code Review Checklist
## API 
- [ ] Return status code properly 
  - Bad Request: The request could not be understood by server due to malformed syntax
  - Not Found: The requested resource could not be found
  - Internal Error
- [ ] Follow the API doc in avx2-openapi-documentation repo 
  - Regular Error 
  - Succeeded
- [ ] Not expose sensitive information to end user
    - Database error returned by db layer
## Go Standard / Best Practice
- [ ] Follow Go standard naming convention 
  - MixedCaps
- [ ] Error strings is not capitalized
- [ ] Sort imported package, redundant newline 
- [ ] Declaring an empty slice
  - Prefer  
```go
    var t []string  
```
over 
```go 
    t := []string{}
```
- [ ] Naming
  - [ ] Function/Method name should avoid repetition
  - [ ] Variable name should be short
  - [ ] Avoid shadowing
- [ ] Avoid over long line
- [ ] Group similar definition
- [ ] Prefix unexported global var by _
- [ ] Embedding struct should be at the top of the field list of struct
- [ ] Prefer `strconv` over `fmt`
- [ ] Avoid string to byte conversion 

## Common
- [ ] Use slice-indexing/switch-case when possible to search/map data
- [ ] KISS
- [ ] Should not have EOF error
