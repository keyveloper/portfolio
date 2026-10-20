# 체험단 플랫폼

회원, 게시글, 이미지, 좋아요, 팔로우 등으로 서비스를 분리한 Spring Boot 기반 MSA 프로젝트입니다. 서비스 개발과 함께 인증·스토리지 이전, AWS EKS 배포 환경 구성을 진행했습니다.

[포트폴리오 목록으로 돌아가기](../README.md)

## 개발 범위

1인 프로젝트로 서버, 웹·Android 클라이언트 및 클라우드 배포 구성을 개발했습니다.

## 주요 구현 내용

- **인증 체계 전환:** Spring Security 기반 인증을 AWS Cognito로 이전하여 토큰 관리를 위임했습니다.
- **이미지 저장 구조 개선:** 로컬 저장소를 S3 중앙 스토리지로 전환하고 게시글·이미지 연결 및 썸네일 생성 기능을 구현했습니다.
- **웹 전송 최적화:** CloudFront 캐싱과 gzip 압축을 적용했습니다.
- **EKS 네트워크 구성:** Public·Private 서브넷을 분리하고 ALB 라우팅, VPC Endpoint를 통한 S3·ECR 연동을 구성했습니다.
- **GitOps 배포:** GitHub Actions와 ArgoCD를 활용한 배포 파이프라인을 구성했습니다.

## 기술

Kotlin, Spring Boot, Node.js, React, Jetpack Compose, MySQL, AWS S3, DynamoDB, Cognito, SNS, SQS, Lambda, EKS, ECR, GitHub Actions, ArgoCD, Helm

## 소스 코드

| 구성 | 저장소 |
| --- | --- |
| 프론트 서버 | [Spring-Marketing](https://github.com/keyveloper/Spring-Marketing) |
| 인증 API | [marketing-auth-api-server](https://github.com/keyveloper/marketing-auth-api-server) |
| 이미지 API | [marketing-image-api-server](https://github.com/keyveloper/marketing-image-api-server) |
| 좋아요 API | [marketing-like-api-server](https://github.com/keyveloper/marketing-like-api-server) |
| 팔로우 API | [marketing-follow-api-server](https://github.com/keyveloper/marketing-follow-api-server) |
| 알림 API | [marketing-noti-api-server](https://github.com/keyveloper/marketing-noti-api-server) |
| 타임라인 API | [marketing-timeline-api-server](https://github.com/keyveloper/marketing-timeline-api-server) |
| 사용자 프로필 | [marketing-user-profile-server](https://github.com/keyveloper/marketing-user-profile-server) |
| 웹 클라이언트 | [marketing-web](https://github.com/keyveloper/marketing-web) |
| Android 클라이언트 | [Compose-Marketing](https://github.com/keyveloper/Compose-Marketing) |
| GitOps 배포 구성 | [marketing-gitops-document](https://github.com/keyveloper/marketing-gitops-document) |
