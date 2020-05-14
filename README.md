[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
<img src="src/main/resources/static/images/logo_transparent.png" width="200" align="right" />

# Клюкарник
Целта на тази задача е да създадем един клюкарник, където всеки може да праща клюкини и да следи клюкините на своите приятели.

## Компилиране
За компилиране на проекта се нуждаете от maven.

## REST API спецификация
След стартиране на проекта, отворете http://localhost:8080/api/index.html
за да видите спецификация на REST API, които трябва да направите.

## Изисквания
1. Направете [fork](http://ext4.codix.eu/jprogrammers/season-1/GOSSIP-TALKS/forks) на repository-то за вашият екип.
1. Приложението трябва да прави това, което е описано във API.
1. `mvn verify` трябва да минава без проблеми (проекта е конфигуриран да изисква 50% code coverage).
1. Spotbugs е maven plugin, който ще ви помогне да създадете качествен код. Като част от условието на задачата е този пългин да не отчита проблеми в кода.
1. Можете да добавяте колко си искате още библиотеки, и maven plugins, но без да премахвате вече избраните.
1. Кода трябва да е форматиран използвайки [Google Style Guide](https://github.com/google/styleguide/)


## Бележки
`api.yml` - документацията на REST API е създадено с помощта на http://editor.swagger.io. Всъщност се използва [OpenAPI](https://swagger.io/docs/specification/about/) формат.

## Web Приложение
Web приложението е достъпно като отворите http://localhost:8080 в web browser.

To е разработено с помощта на mock server. За стартирането му е нужно:
1. Да имате инсталиран docker.
2. Да пуснете следният команден ред в `src/main/resources/static`:
```shell script
docker run -p 8000:8000 -v `pwd`/api.yml:/api.yml danielgtaylor/apisprout --validate-server /api.yml  
```


## Документация
За информация относно използваните библиотеки и инструменти:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.2.6.RELEASE/maven-plugin/)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.2.6.RELEASE/reference/htmlsingle/#boot-features-developing-web-applications)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.2.6.RELEASE/reference/htmlsingle/#boot-features-jpa-and-spring-data)

## Ръководства
Следните ръководства илюстрират как да използвате Spring:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

