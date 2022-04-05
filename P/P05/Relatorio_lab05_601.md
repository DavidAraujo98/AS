# Lab 05 - Architecture of Views

## Grupo - **601**

| Membros | Número Mecanográfico |
| :- | :-: |
| Daniel Capitão | 75943 |
| <u>David Ferreira</u> | 93444 |
| Samuel Teixeira | 103325 |
| Filipe Costa | 77548 |

## Exercício 5.1
### a)
The displayed diagram shows us a simplified view of a few component that we might encounter in Blogging services.

There are four components three of which expose interfaces to other components. The *BlogDataSource* which probably maintains the all the blogs information will require an external **logging** component which will be responsible for the authentication, for that the component will require the interface ***Logger*** exposed by the component *Log4j*.

The next component is the *ConversionManagement*, this component, according with the Diagram 1, is responsible for managing the blog's post, and to do soo. it will require a interface to access the data source provided by the *BlogDataSoure* component. Once the information is handled, the component will expose to different interfaces to access this data.

One of this interfaces, *FeedProvider*, seems to provide a RSS feed soo the Blog posts are accessible via any RSS Feed reader (ex: Feedly), this interface will be required by the ***BrodcastEngine*** which will probably be responsible to propagate this RSS feed.

The second interface, *DisplayConverter*, seems to make this blog post accessible in a somewhat normal text format, which the component ***BlogViewer*** will require in order to, probably, post the blog's content into the blog's website.

### b)

The Apache Log4j component is a Java-based utility for logging. What is does in a "plugin" type utility for an external service to use for user authentication into the system, this is practical in the sense that the developer does not need to create a new authentication scheme from zero and just implements this module to the project.

### c)

```h
//
https://mvnrepository.com/artifact/org.apache.logging.log4j/log4j-core
implementation group: 'org.apache.logging.log4j', name: 'log4j-core', version: '2.17.2'
````

<div style="page-break-after: always;"></div>

## Exercício 5.2

![P5-5.2](P5-5.2.drawio.png)

<div style="page-break-after: always;"></div>

## Exercício 5.3

### a)

![P5-5.3_a)](P5-5.3a.drawio.png)

### b)

![P5-5.3_b)](P5-5.3b.drawio.png)