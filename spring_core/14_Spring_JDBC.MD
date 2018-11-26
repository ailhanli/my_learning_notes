Spring Jdbc Integratition

Spring jdbctemplate clean down our code dramatically.
there is a mechanism in jdbc use but diffuclt to use it. There is error code coming from exception class. it is vendor dependent. so running same code different db will code fails

in jdbc template ex is internally and automatically catched  it checks error codes for many databases and throw meaningfull runtime exception. These exceptions are unchecked. programmer error.

During the DAO implementation, DAO method names can be simple as CRUD but on the service side we need to give meaningful name for customer for example on DAO you can give the name insertCustomer for new customer you have to give service as newCustomer. It is same also for exception throwing. Normally we don’t need to handle exceptions by default, but for example find, delete, update method need record_not_found exception. On the DAO level customer exception should be dao specific for example RecordNotFoundException, on the service layer it should be CustomerNotFoundException. For example If we have Customer-Call relationship we can add on DAO level as newCall but we have to add on service level recordCall.

On note that; for adhere Single Responsibility Principle we need to create new DAO for every domain object and new Service for every domain. In case for example we have accountService and bookService. We need to use book service for querying and accountService for billing on this time we need to create new Service it name is PurchaseService.



