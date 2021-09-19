
---
layout: post
title:	"스프링부트 어노테이션"
date:	2021-08-15 12:00:00
categories:
    - blog
tags:
    - springboot
---

어노테이션이란   
쉽게 설명하자면 프로그램에게 추가적인 정보를 제공해주는 메타데이터이다   
***
어노테이션의 죵류

```java
@SpringBootApplication
/*
이 어노테이션 안에는 3가지 중요한 어노테이션이 있다
Configuratin 기능을 하는 @SpringBootConfiguration
자동으로 scan하여 빈을 등록하는 @ComponentScan 
스프링부트의 메타데이터를 빈으로 등록하는 @EnableAutoConfiguration이 있다
*/
@GetMapping
@RequestMapping
//데이터를 가져올 때 사용(Get은 메소드에만 적용)
@RequiredArgsConstructor
//초기화 되지않은 필드에 대해생성자를 생성해 줌
@Data
//여러 Lombok 어노테이션을 한번에 설정할수있음
@Getter
@Setter
//말그대로 getter와 setter함수를 생성

```

