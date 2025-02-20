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
