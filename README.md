# MSA 맛보기 👅
![architecture](./docs/images/monolith-microservices.png)
*출처: https://aws.amazon.com/ko/compare/the-difference-between-monolithic-and-microservices-architecture/*

## What is MSA(Microservices Architecture)?
- 각 기능을 독립적인 서비스로 분리하고, 분리된 서비스들을 서로 통신하게 설계하는 구조이다.

### What is MSA advantages?
- 분리된 서비스별로 개별 배포가 가능하여 빠른 개발 및 배포가 가능하다.
- 서비스마다 적절한 기술 선택이 가능하다.
- 스케일 아웃 시, 전체 애플리케이션에 리소스를 추가할 필요 없이, 확장이 필요한 서비스에만 추가하면 된다. (비용 감소!)
- 하나의 서비스에 장애가 발생해도 다른 서비스는 정상적으로 운영될 수 있다.
---

## Example: Ticketing

### Service
1. 공연 정보 서비스
2. 예매 서비스
3. 결제 서비스
4. 알림 서비스

### if Monolithic Architecture
- 인기 가수의 티켓 오픈 시간에는 예매 서비스에 트래픽이 매우 몰릴 것  
-> 예매 서비스에만 트래픽이 몰린 거지만, 모든 서비스가 하나의 애플리케이션에서 동작되기 때문에 다른 서비스(공연 정보 서비스, 결제 서비스)까지 영향을 받아, 전체적으로 느려질 수 있다.

### Microservices Architecture
- 예매 서비스에만 트래픽이 몰려도 다른 서비스는 정상적으로 동작할 수 있다.
- 예매 서비스만 스케일링이 가능하여, 비용을 줄일 수 있다.
- 예매 서비스에 장애가 발생해도, 다른 서비스는 영향을 받지 않는다.



