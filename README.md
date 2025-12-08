### Data_Engineering_Articles

`Setting the scene`
As you go through this material, picture yourself as new data engineer hire in your organization. Your task will be to understand the needs of your stakeholders as first principles approach to understanding and translating the needs of the buiness into technical solutions  

This is a journal of my self-study and research on Data Engineering and its Ecosystem

## What is Data Engineering?
Data Engineering is the development, implementation, and maintenance of systems and processes that take in raw data (generate and ingest), transforms it and produce high-quality consistent information that supports downstream use cases.

### Data Engineering Lifecycle: The core stages of the data engineering lifecyle are as follows:
- `Generation`:
  * The data used in the data engineering lifecyle originates within/from source systems.For example, a source system could be an IOT device, an application message queue, or a transactional database. A data engineer needs to have a working knowledge of how a given source system operates, generates its data, the frequency, velocity
    and variety of the data it generates. Engineers need to maintain a line of communication with source systems owners to stay up-to-date on changes that can impact data pipelines and analytics.
     - `The following questions can be asked to evaluate a source system:`
     - What are the essential characteristics of the data source? Is it an application? or A swarm of IoT devices?
     - Does the data persist long term or short term before deletion?
     - What is the speed of generation and what are the rate of errors, if any?
     - What is the schema of the ingested data?
     - How frequently should data be pulled from the source system?
     - Will reading from a data source impact its performance?
- `Storage`:
  * Choosing a storage solution is key to success across the rest of the data lifecycle. Storage is also one of the more complicated stages of the lifecycle for a number of reasons. First is that cloud storage solutions often requires use of more than a single source of truth. Storage solutions are rarely exclusively purposed for 
    storage. They can be used for transformation capabilities as well. Amazon S3 select is good example of this. While storage is a phase of the data engineering lifecycle, it frequently touches on other stages, such as ingestion, transformation, and serving. In many ways, the way data is stored impacts how it is used in all of the 
    stages of the data engineering lifecyle. For instance, cloud warehouses can store data, process data in pipelines, and serve it to analysts. Streaming frameworks such as Apache Kafka, and Pulsar can ingest, store and query systems for messages, with object storage being a standard layer for data transmission.

        Understanding Data Access Frequency:
         * Data retrieval patterns will vary based on the data being stored and how often it is queried. Data access frequency will determine the temperature of the data. Data that is most frequently accessed is known as `hot data`.
           Hot data is commonly retreived multiple times per day. For example, systems that service user requests
           CRM systems, ticketting systems etc. And then, there is `lukewarm data` and `cold data` that are less frequently accessed.
-  `Ingestion`:
      * Source systems and Ingestion presents the most significant bottle-necks of the data engineering lifecycle. This is because the engineer has little to no control of the management of these two processes. Unreliable source and ingestion systems have ripple effects across the data engineering lifecyle. To architect and build a system, the following considerations are critical to keep in mind:
        - What are the use cases for the data being ingested? Is the data good for reuse rather than creating multiple versions of the same dataset?
        - How frequently will the data be accessed?
        - Is the data being reliably generated and available on demand?
        - In what volume will the data typically arrive?
        - What format is the data in? Can your downstream storage and transformation systems handle this format?
        - Is the source data in good shape for immediate downstream use? And for how long?
-  Transformation
-  Serving

  There is also the notion of `undercurrents` - these are critical themes and concepts around the end-to-end lifecycle. These include the following
- Security
- Data Management
- DataOps
- Data Architecture
- Orchestration
- Software Engineering

## Concept of Data Maturity: 
Data Maturity is the progression from basic towards advanced data utilization, capabilities, and integration across the organization. An Organization's Data Maturity is not a factor of the age or revenue of a company. Typically companies fall within one or more of these stages on their data maturity evolution
- `Starting with Data`
- `Scaliing with Data`
- `Leading with Data`

In general, the role of a data engineer evolves from a generalist to a specialist as an organization advances through these stages of the data maturity model.

## Business Responsibilites of a Data Engineer
- Understand how to scope and gather business and product requirements
- Know how to communicate with nontechnical and technical people
- Understand the foundations of Agile, DevOps and DataOps
- Control Costs
- Learn Continuously

A successful data engineer always zooms out to understand the big picture and how to achieve outsized value for the business.

## Technical Responsibilities of a Data Engineer
At a high level, data engineers must understand how to build architectures that optimize performance and cost, using using off-the-shelf and proprietary components. The primary languages of data engineering are 
- `SQL`
- `Python`
- `Java` or `Scala`
- `Bash`
- `R`

The reality of the industry is that data engineers are most often than not required to understand the fundamentals of software engineering; sometimes even required to be software engineers. Thus data engineers may need to develop proficiency in secondary programming languages, including R, JavaScript, Go, Rust, C/C++, c# and Julia. 

As far as keeping ones skills sharp in a rapidly changing field like data engineering ? A good approach is to start by focusing on the fundamentals to understand what's not going to change and pay attention to ongoing developements to know know where the field is headed. 

## Notion of Type A and Type B Data Engineers

*Type A ~ Abstraction ~ Data Engineers* 

These types of data engineers in their roles avoid undifferentiated heavy lifting, keeping data architecture as abstract and straightforward as possible and not reinventing the wheel. In practice, they do not attempt to reinvent the wheel and leverage off-the-shelf products and managed services and tools. 

*Type B ~ Build ~ Data Engineers*

These types of data engineers build data tools and systems that scale and leverage a company's core competency and competitive advantage. Type A and B data engineers may work in the same company and at times may or may not be the same person!

I'm Back. Let's PICK FROM WHERE WE STOPPED :--





