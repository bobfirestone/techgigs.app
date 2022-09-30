# techgigs.app

TechGigs.app is a marketplace for tech workers to pick up side gigs

## User Journey

```mermaid
journey
  title post the gig
    post wizard: 1 : poster
    pay for posting: 1: poster
    search for gigs: 1 : freelancer
```

```mermaid
journey
  title contract the gig
    message poster: 1 : freelancer
    negotiate details: 1 : poster, freelancer
    fill in contract: 1 : poster
    sign the contract: 1 : poster, freelancer
```

```mermaid
journey
  title work the gig
    do the work: 0 : freelancer
    submit change order: 1 : freelancer
    sign off on change order: 1 : poster
```

## Data Diagram

```mermaid
classDiagram

User <|-- Profile
User <--> Messages

User --> Employeer
Employeer --> Listing
Employeer -- Credit
Credit --> Listing
Contract --> Listing
Contract --> Employeer
Contract --> User
Contract --> ContractDetails
Contract --> ChangeOrders

Listing --> ProjectType
Listing --> Technology
ProjectType --> ProjectSuperType
Technology --> TechnologyClass

User : int id
User : string email
User : string password

Employeer: int id
Employeer: string name
Employeer: array int user_ids
Employeer: text about_us
Employeer: string logo_url

Profile : int user_id
Profile : text biography
Profile : text location

Messages : int id
Messages : int to_id
Messages : int from_id
Messages : text body
Messages : bool read

Credit : int user_id
Credit : int listing_id

Listing : int id
Listing : string title
Listing : test description
Listing : bool active
Listing : array technologies
Listing : int project_type

Contract : int id
Contract : int listing_id
Contract : int worker_user_id
Contract : datetime worker_signed_at
Contract : int employer_user_id
Contract : datetime employer_signed_at

ContractDetails : int id
ContractDetails : datetime created_at
ContractDetails : text description_of_services
ContractDetails : text deliverables
ContractDetails : text project_schedule
ContractDetails : text pricing_and_rates
ContractDetails : text payment_terms_and_schedule
ContractDetails : text terms_and_conditions
ContractDetails : datetime locked_at
ContractDetails : bool locked

ChangeOrders : int id
ChangeOrders : text changes
ChangeOrders : datetime accepted_at
ChangeOrders : int accepted_by_id
ChangeOrders : int created_by_id


ProjectType : int id
ProjectType : string super_type_id
ProjectType : string type
ProjectType : string platform
ProjectType : name()

ProjectSuperType : int id
ProjectSuperType : string name

Technology : int id
Technology : string name
Technology : string icon
Technology : int technology_class_id

TechnologyClass : int id
TechnologyClass : type

```

### ProjectType

| super type         | type     | platform       |
| ------------------ | -------- | -------------- |
| software           | desktop  | cross platform |
| software           | desktop  | macOS          |
| software           | desktop  | windows        |
| software           | desktop  | linux          |
| software           | mobile   | iOS            |
| software           | mobile   | android        |
| software           | mobile   | cross platform |
| software           | web      | full stack     |
| software           | web      | backend        |
| software           | web      | frontend       |
| design             |          |                |
| design             | app      |                |
| design             | branding |                |
| design             | logo     |                |
| design             | print    |                |
| design             | website  |                |
| project management |          |                |
| DevOps             |          |                |
| DevOps             | CI/CD    |                |
| Hardware           |          |                |
| Hardware           | iot      |                |
| Quality Assurance  |          |                |

### TechnologyClass

| classification       |
| -------------------- |
| Programming Language |
| Framework            |
| Database             |
| Cloud Provider       |
| Operations           |

### Programming Languages

- JavaScript
- TypeScript
- ruby
- Go
- python
- rust
- C
- C++
- C#
- Java
- Scala
- Visual Basic
- SQL
- php
- Objective-C
- MATLAB
- Swift
- R
- Perl
- Julia
- Lua
- Scala
- Kotlin
- elixir
- erlang
- crystal

### Frameworks

### Data Store

- postgresql
- MySql
- MarisDB
- oracle
- MS sql server
- MongoDB
- IBM DB2
- Redis
- Elasticsearch
- Cassandra
- OrientDB
- SQLite
- DynamoDB
- Neo4j
- Firebase
- FileMaker
- Microsoft Access

### Cloud Providers

- Amazon Web Services
- Google Cloud Platform
- Microsoft Azure
- Digital Ocean
- Heroku

### Operations

- Docker
- Kubernetes
- Github Actions
- Gitlab DevOps
