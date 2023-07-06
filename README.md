# Exchange Crypto Market

Exchange Crypto Market is a cryptocurrency trading platform that allows users to buy and sell various cryptocurrencies. 
It provides real-time market data, trading functionality, and secure wallet management.

The application is under development in a microservice architecture. If you want to look at the mono version:

https://github.com/Coriv/SenseiMarket

## Features

- User Registration and Login
- Cryptocurrency Listings
- Real-Time Market Data (from Binance API)
- Real-Time exchange USD - PLN rate (from NBP API)
- Trading (Buy/Sell)
- Transaction History
- Wallet Management
- Account Balance and Portfolio Tracking
- User Dashboard

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

## Setup

1. Clone the repository:
   git clone https://github.com/Coriv/Exchange-Crypto-Market.git
2. Set databases for services according to bootstrap.properties files
3. Run first three services in the order listed:
   - Server Config
   - Server Discovery
   - Gateway
   Then you can run another one in any order.

## Development plans

1. Add service for storing transaction history
2. Add service to binance api support
3. Add tests to controllers
4. Add swagger and update readme.md with shots of endpoints
