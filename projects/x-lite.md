# x-lite 플랫폼

회원, 게시글, 타임라인, 알림, 좋아요, 팔로우 기능을 제공하는 Java·Kotlin 기반 MSA 프로젝트입니다. 서버 개발과 메시지 처리, 배포 자동화, 운영 모니터링을 경험하기 위해 진행했습니다.

[포트폴리오 목록으로 돌아가기](../README.md)

## 개발 범위

1인 프로젝트로 진행했으며 1:1 멘토링을 병행했습니다. Spring Boot 서버와 컨테이너·클라우드 운영 환경을 구성했습니다.

## 주요 구현 내용

- **서버 개발과 인증:** Spring Boot로 서비스를 개발하고 Spring Security·JWT 기반 인증을 적용했습니다.
- **알림 처리 안정성:** Kafka 클러스터를 도입하고 DLQ와 지수적 백오프를 적용하여 메시지 처리 실패에 대응했습니다.
- **통합 모니터링:** ELK와 Prometheus·Grafana를 활용해 분산된 로그와 메트릭을 통합 모니터링했습니다.
- **배포 자동화:** Jenkins 기반 CI/CD, Docker 컨테이너화, ArgoCD 기반 GitOps 배포를 구성했습니다.
- **클라우드 운영:** AWS EKS와 관련 인프라를 구성하며 서비스 배포와 통신 문제를 다뤘습니다.

## 기술

Java, Kotlin, Spring Boot, Spring Security, JWT, MySQL, Kafka, JUnit5, Swagger, Jenkins, GitHub Actions, Docker, Kubernetes, EKS, ArgoCD, Terraform, ELK, Prometheus, Grafana

## 소스 코드

| 구성 | 저장소 |
| --- | --- |
| 프론트 서버 | [X-FrontServer](https://github.com/keyveloper/X-FrontServer) |
| 좋아요 API | [X-LikeApiServer](https://github.com/keyveloper/X-LikeApiServer) |
| 타임라인 API | [X-TimelineApiServer](https://github.com/keyveloper/X-TimelineApiServer) |
| 알림 API | [X-NotiApiServer](https://github.com/keyveloper/X-NotiApiServer) |
| 인프라 및 배포 구성 | [devops-management](https://github.com/keyveloper/devops-management) |
