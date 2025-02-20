## 주요 링크

- S3 버킷 웹사이트 엔드포인트: [S3 앤드 포인트](http://frontend-4th-chapter-4-1.s3-website.ap-northeast-2.amazonaws.com)
- CloudFrount 배포 도메인 이름: [CloudFrount 배포 도메인](https://d2jowg7kbhchxv.cloudfront.net)

## 주요 개념

- GitHub Actions과 CI/CD 도구:

  - GitHub에서 제공하는 자동화된 워크플로우 도구
  - 코드를 푸시하면 자동으로 테스트, 빌드, 배포 등을 수행
  - .github/workflows/deployment.yml에 로직 작성

- S3와 스토리지:

  - 정적 웹사이트 호스팅, 대용량 파일 저장 등에 활용
  - 파일을 버킷이라는 단위로 저장

- CloudFront와 CDN:

  - CloudFront는 AWS의 CDN(Content Delivery Network)
  - 전 세계 엣지 로케이션에 콘텐츠를 캐싱해서 사용자에게 가까운 위치에서 빠르게 콘텐츠를 제공

- 캐시 무효화(Cache Invalidation):

  - CDN에 캐싱된 콘텐츠를 강제로 삭제하는 작업
  - 웹사이트가 업데이트되었을 때 사용자들이 최신 버전을 볼 수 있도록 기존 캐시를 무효화해야 함
  - 파일명에 해시를 추가해서 로컬 캐시도 무효화 할 수 있음

- Repository secret과 환경변수:
  - GitHub 레포에서 안전하게 관리되는 비밀값

## CDN 성능 비교 분석 보고서
### 1. 개요
S3 정적 호스팅과 CloudFront CDN 배포 방식의 성능을 TTFB 중심으로 비교 분석한 결과입니다.
### 2. 테스트 환경
- 위치: 아시아 태평양(서울)
- 원본 서버:  AWS ap-northeast-2
- 테스트 환경: 데스크톱
- CDN 서비스: Amazon CloudFront

### 3. 성능 비교
#### S3 직접 배포
- 사이트 크기: 12.5KB
- TTFB: 30.87ms

#### CloudFront 배포
- 사이트 크기: 3.2KB
- TTFB: 21.41ms

### 4. 성능 개선 효과
    
### 5. 결론
- TTFB: 30.6% 감소
- 사이트 크기: 74.4% 감소

이러한 결과는 CloudFront CDN이 웹 서비스의 성능 향상에 매우 효과적임을 보여줍니다.
