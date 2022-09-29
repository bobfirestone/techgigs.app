# techgigs.app

TechGigs.app is a marketplace for tech workers to pick up side gigs

```mermaid
classDiagram

User <|-- Profile
User <--> Messages
User --> Credit
User --> Listing
Credit --> Listing

Listing --> ProjectType
Listing --> Technology
Technology --> TechnologyClass

User : int id
User : string email
User : string password

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

ProjectType : int id
ProjectType : string name

Technology : int id
Technology : string name
Technology : string icon
Technology : int technology_class_id

TechnologyClass : int id
TechnologyClass : type

```

### ProjectType

| type    | platform       |
| ------- | -------------- |
| desktop | cross platform |
| desktop | macOS          |
| desktop | windows        |
| desktop | linux          |
| mobile  | iOS            |
| mobile  | android        |
| mobile  | cross platform |
| web     | full stack     |
| web     | backend        |
| web     | frontend       |

### TechnologyClass

| class                |
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
