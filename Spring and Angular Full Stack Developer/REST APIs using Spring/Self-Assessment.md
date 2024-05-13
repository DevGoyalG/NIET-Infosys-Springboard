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
