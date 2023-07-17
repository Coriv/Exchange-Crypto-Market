# Exchange Crypto Market

Exchange Crypto Market is a cryptocurrency trading platform that allows users to buy and sell various cryptocurrencies. 
It provides real-time market data, trading functionality, and secure wallet management.

The application is under development in a microservice architecture. If you want to look at the mono version:

https://github.com/Coriv/SenseiMarket

## Technologies Used

- Java
- Spring Framework
- Hibernate
- MySQL
- Spring Cloud
- Spring Security
- Spring Web
- JWT authentication
- RabbitMQ
- Docker
- JMS
- JUnit
- Mockito
- Swagger (with the nearest update)
- Spring AOP (with the nearest update)

## Features
- Server Discovery allows to register services and find them

      https://github.com/Coriv/ServerDiscoveryCM
- Server Config provides configuration for services

      https://github.com/Coriv/ServerConfigCM
- Gateway directs requests to appropriate services, calls authService

      https://github.com/Coriv/GatewayCM
- UserService allows to user registration
                        
      https://github.com/Coriv/UserService
- AuthService allows to authenticate users requests 

      https://github.com/Coriv/AuthService
- Cryptocurrency contains a list of cryptocurrencies allowed for trading 

      https://github.com/Coriv/CryptocurrencyCM
- Wallet service allows to cash management, deposit and withdraw funds

      https://github.com/Coriv/Wallet/
- WalletCrypto service allows to management our cryptocurrency, deposit and withdraw them

      https://github.com/Coriv/WalletCrypto/
- Trade service allows you to sell and buy crypto

      https://github.com/Coriv/Trade/
- Email service sends notifications to users

      https://github.com/Coriv/EmailService

## Setup

1. Clone the repository:
   git clone https://github.com/Coriv/Exchange-Crypto-Market.git
2. Set databases for services according to bootstrap.properties files
3. Run services in the following order:
   - Server Config
   - Server Discovery
   - Gateway
   Then you can run another one in any order.

## Development plans

1. History  that storing transaction history, both cash and cryptocurrency
2. Binance service that downloads data on cryptocurrency prices from external API
3. Update Trade Service to send notification by EmailService about new offers
4. Swagger and update readme.md with shots of endpoints


## Useful Endpoints

All endpoints listed below point to gateway

### User Service

- `POST /v1/user`: Create a new user.
    - Request Body: UserDto
    - Response: ResponseEntity<String>

This call will create a new user, authService account, cash wallet and crypto wallets

### Trade Service

- `POST /v1/trade`: Create a new trade.
    - Request Body: CreateTradeDto
    - Response: ResponseEntity<TradeDto>

- `GET /v1/trade`: Fetch open trades (optional by symbol).
    - Query Parameter: symbol (optional)
    - Response: ResponseEntity<List<TradeDto>>

- `DELETE /v1/trade/{tradeId}/delete`: Delete a trade.
    - Path Parameter: tradeId
    - Response: ResponseEntity<Void>

- `PUT /v1/trade/{tradeId}`: Execute a trade.
    - Path Parameter: tradeId
    - Request Body: TradeDealDto
    - Response: ResponseEntity<CreateTradeDto>


