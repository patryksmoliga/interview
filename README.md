# interview

Our aim is to create an application to manage user bank account.
Bank account consits of data such as: accountNumber, userId, balance, homeCity
Tasks:
1. Add endpoint that will allow to transfer money to other account. Input for your endpoint is sourceAccountNumber as path param and body {"amount":1000, "targetAccountNumber:"PL65109024024837322687773932"}
You should fetch both accounts, take money out of source account and add it to the target account.
You don't have to implement repository part, you can leave it as service with empty methods.
You should not allow for transfer if user performing operation is not owner of the account. Create UserService with method getCurrentUserId(){return 123;}
Write unit tests.

2. We need to validate each money transfer if it is fraudulent operation. Now your input is {"amount":1000, "targetAccountNumber:"PL65109024024837322687773932", "userCurrentLocation": "Wrocław"}. You should not allow for transfer when transfer amount is higher than 15 000 and userCurrentLocation is different than his homeCity.
Write unit tests. 

3. Previously we accepted only operations in PLN currency, but now we want to support also different currencies, how can we add such feature ?

4. We assume that operation is fraudulent when it is second transfer to the same account for over 10 000 within 24 hours. How can we implement it?
{"amount":1000, "targetAccountNumber:"PL65109024024837322687773932", "userCurrentLocation": "Wrocław", "transferDate": "19.09.2024T22.45"}


Additional questions:
1. 
How can we put some restricions on input data when we recieve it via API endpoint?
Do you know what are validation groups?
What is @Transactional annotation, how it works? Czy zabranie i dodanie kasy powinno byc ujete w transakcje? Co sie stanie jezeli tego nie zrobimy?
Jaki kod bledu zwrocisz gdy user nie jest wlascicielem konta ?
W jaki sposob mozemy obslugiwac wyjatki w javie ?
W jaki sposob mozemy mapowac wyjatki na kody http w springu? 

2. Jaki kod bledu zwrocisz w takiej sytuacji?


3. Co to sa niezmienniki?
