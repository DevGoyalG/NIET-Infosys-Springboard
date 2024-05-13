Q1 of 20

What is the by default URL for the Spring Security login page?

- [x] ***/login***
- [ ] /signin
- [ ] /auth
- [ ] /index

Q12 of 20

Which of the following statements are true regarding Matrix variables? (Choose any 2 options)

- [x] ***We cannot use Matrix Variables in URI without required configuration.***
- [ ] Matrix variables should always be to the end of URI
- [x] ***We separate matrix variables by Semi colon ";"***
- [ ] Matrix Variable should always be of type Map as it has to hold key, value pairs.


Q5 of 20

Have a look at the following controller method. (Assume that the REST resources corresponding to employee and address are available in the same application.)

@PostMapping()
public string createEmployee (@RequestBody EmployeeDTO empdto) {
    Rest Template restTemplate = new RestTemplate();
    string url = "http://localhost:8080/address/{phoneno}";
    Long Phoneno-9897969543L;
    //Line 1
    //code to insert employee in table
}

What should be inserted at Line 1 to invoke another controller method with URL http://localhost:8080/address/{phoneno} to get the latest address details which are used in adding employee data to the table.

- [ ] Address response = restTemplate.exchange(url, HttpMethod.Get, phoneno);
- [x] ***ResponseEntity<Address> response = restTemplate.exchange(url, HttpMethod.Get, null, Address.class, phoneno);***
- [ ] Address response = restTemplate.getForEntity(url, phoneno);
- [ ] ResponseEntity<Address> response = restTemplate.getForObject(url, Address.class, phoneno);
