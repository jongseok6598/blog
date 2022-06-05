---
layout: post
title:	"Spring DTO,DI,IOC"
date:	2021-10-24 12:00:00
categories:
    - blog
tags:
    - springboot
---
DTO란   
계층간 데이터 교환을 위해 사용하는 겍체다   
DB의 데이터를 Service나 Controller 등으로 보낼 때 사용하는 겍체를 말한다

예
```java
@Getter 
@Setter
class ArticleDTO {
  private String title;
  private String content;
  private String writer;
}
```
***
DI   
의존성 주입, 겍체를 직접 생성하는 게 아니라 외부에서 생성한 후 주입 시켜주는 방식   
의존성 주입 방법   
1. 생성자를 이용   
```java
@Service
public class Service {

    private Repository repository;

    public BugService(Repository repository){
        this.Repository = repository;
    }
}
```
2. 필드변수를 이용   
```java
@Service
public class Service {
    @Autowired//필요한 의존 객체의 “타입"에 해당하는 빈을 찾아 주입
    private Repository repository;
}
```
3. setter를 이용
```java
@Service
public class Service {

    private Repository repository;

    @Autowired
    public void setBugRepository(Repository repository) {
         this.Repository = repository;
    }
}
```
***
IoC(Inversion of Control)   
일반적인 의존성에 대한 제어권   
개발자가 직접 의존성을 만든다   
예
```java
public class OwnerController {
	private OwnerRepository ownerRepository = new OwnerRepository();
}
```




