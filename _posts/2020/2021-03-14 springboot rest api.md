---
layout: post
title:	"Spring rest api"
date:	2021-03-14 12:00:00
categories:
    - blog
tags:
    - springboot
---
Springboot api만드는법         
1. 컨트롤러 요청   
```java
    @GetMapping(value = "/api/carList")
    public ArrayList<HashMap> returncarList(){
        return testService.makeCarJsonList();
    }
```
2. 서비스에서 로직 처리   
```java
    public ArrayList<HashMap> makeCarJsonList() {
        HashMap<String,String> car1 = new HashMap<>();
        car1.put("id","1");
        car1.put("model","A4");
        car1.put("company","audi");

        HashMap<String,String> car2 = new HashMap<>();
        car2.put("id","2");
        car2.put("model","A7");
        car2.put("company","audi");

        HashMap<String,String> car3 = new HashMap<>();
        car3.put("id","3");
        car3.put("model","C-class");
        car3.put("company","benz");

        HashMap<String,String> car4 = new HashMap<>();
        car4.put("id","4");
        car4.put("model","sonata");
        car4.put("company","hyundai");

        HashMap<String,String> car5 = new HashMap<>();
        car5.put("id","5");
        car5.put("model","K5");
        car5.put("company","kia");

        ArrayList<HashMap> retrunData = new ArrayList<>();
        retrunData.add(car1);
        retrunData.add(car2);
        retrunData.add(car3);
        retrunData.add(car4);
        retrunData.add(car5);


        return retrunData;
    }
```
3. 실행하고 결과가 잘 나왔는지 확인하기
```json
[
    {
        "model": "A4",
        "company": "audi",
        "id": "1"
    },
    {
        "model": "A7",
        "company": "audi",
        "id": "2"
    },
    {
        "model": "C-class",
        "company": "benz",
        "id": "3"
    },
    {
        "model": "sonata",
        "company": "hyundai",
        "id": "4"
    },
    {
        "model": "K5",
        "company": "kia",
        "id": "5"
    }
]
```

