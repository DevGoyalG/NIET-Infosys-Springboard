Q1 of 20

Consider the following controller:

@RestController  
@Valid  
@RequestMapping("accounts")  
public class AccountController {  
    @Autowired  
    private Account Service acctService;  
    @GetMapping("/account")  
    public List<AccountDTO> getAccount Details (@Max (value-10000000, message="the value is out of range") @NotEmpty (message="account number should not  
        return acctService.fetchAccount Details (acctNo, ifsc Code);  
    }  
}  

What is wrong with above controller?

- [ ] @Valid is a parameter level annotation. It should be placed before acctno Request parameter.
- [x] ***@Validated annotation should present over controller rather than @Valid annotation.***
- [ ] There is no wrong with this controller.
- [ ] Should not apply two validations on acctno Request parameter.


Q1 of 20

What is the by default URL for the Spring Security login page?

- [x] ***/login***
- [ ] /signin
- [ ] /auth
- [ ] /index

Q3 of 20

What should be inserted in Line 1, Line 2 to differentiate given controller methods using Request Parameter versioning

//Linel
public PlanDTO fetchPlanById(@PathVariable("planId") int planId)
//Line 2
public string fetchPlanById2 (@PathVariable("planId") int planId)

- [ ] Line1 - @GetMapping(value="/{planld}/VER=1")
Line2 - @GetMapping(value="/{planld}/VER=2")
- [ ] Line1 - @GetMapping(value="/{planld)}?ver=1")
Line2 - @GetMapping(value="/{planld)?ver=2" )
- [x] ***Line1 - @GetMapping(value="/{planld}", params = "VER=1")
Line2 - @GetMapping(value="/{planld}", params = "VER=2")***
- [ ] Line1 - @GetMapping(value="/{planld}) @param(ver=1)
Line2 - @GetMapping(value="/{planld}) @param(ver=2)

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

Q8 of 20

Which class in Spring security is used to hash passwords?

- [x] ***PasswordEncoder***
- [ ] PasswordHasher
- [ ] HashEncoder
- [ ] SecureEncoder

Q9 of 20

Which of the below are ways of realizing and implementing SOA?

- [x] ***WebServices***
- [ ] Lisp
- [ ] Perl
- [x] ***Jini***

Q11 of 20

Have a look at the following controller.

@RestController
@RequestMapping("/bikes")
public class BikeController {
    //Line 1
    public List<BikeDTO> getBikeDetails() {
        //List of bikes get returned
    }
    // Line 2
    public string createBike (BikeDTO bike) {
        //bike got created
    }
}

Which of the below options has statements that can be inserted at Line 1, Line 2 for proper working of the controller?

- [ ] Line 1 - @RequestMapping(value = "/detail")
Line 2- @PutMapping("/create")
- [ ] Line 1 - @GetMapping("/detail")
Line 2- @RequestMapping(value = "/create", method = "Post")
- [x] ***Line 1 - @GetMapping("/detail")
Line 2 - @PostMapping()***
- [ ] Line 1 - @RequestMapping(value = "/detail")
Line 2- @PostMapping("/create")

Q12 of 20

Which of the following statements are true regarding Matrix variables? (Choose any 2 options)

- [x] ***We cannot use Matrix Variables in URI without required configuration.***
- [ ] Matrix variables should always be to the end of URI
- [x] ***We separate matrix variables by Semi colon ";"***
- [ ] Matrix Variable should always be of type Map as it has to hold key, value pairs.

Q15 of 20

Observe the following controller. (Assume necessary imports are done)

@RestController
@RequestMapping("/books")
public class BookController {
    @GetMapping("/det/{bookPrice}")
    public List<BookDTO> getBooks (@RequestParam() String bookName, @PathVariable() int bookPrice) { 
        //code to search for books based on book name and cost.
    }
}

Which of the below is the correct URI to invoke the getBooks() controller method?

- [ ] http://localhost:8080/bookstore/books/det/400/bookName=java 
- [ ] http://localhost:8080/bookstore/books/det/bookPrice-400?bookName=java 
- [x] ***http://localhost:8080/bookstore/books/det/400?bookName=java***
- [ ] http://localhost:8080/bookstore/books/det?bookName=java/400

Q16 of 20

Identify the correct order of request processing in Spring Rest.

- [ ] Client, DispatcherServlet, HandlerMapper, Controller, ViewResolver, Client
- [x] ***Client, DispatcherServlet, HandlerMapper, Controller, Client***
- [ ] Client, HandlerMapper, DispatcherServlet, Client
- [ ] Client, HandlerMapper, ViewResolver, DispatcherServlet, Client
