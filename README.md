# Santander Wek 2024 #

## Configurações iniciais da criaçao do projeto ##
### [Link do Spring Initializr](https://start.spring.io/#!type=gradle-project&language=java&platformVersion=3.3.2&packaging=jar&jvmVersion=17&groupId=com.example&artifactId=santander-dev-week-2024&name=santander-dev-week-2024&description=Java%20REstfulAPI%20criada%20para%20a%20Santander%20Dev%20Week%202024&packageName=com.example&dependencies=web,data-jpa,h2,postgresql) ###

## Diagrama de Classes

```mermaid
classDiagram
  class User {
    -String name
    -Account account
    -Feature[] features
    -Card card
    -News[] news
  }

  class Account {
    -String number
    -String agency
    -Number balance
    -Number limit
  }

  class Feature {
    -String icon
    -String description
  }

  class Card {
    -String number
    -Number limit
  }

  class News {
    -String icon
    -String description
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News
```