# 구조
![cicd-project](https://github.com/user-attachments/assets/9a3f1a9d-c719-42cc-91f1-9a0e8db2d3ec)


# 도구
terminus, docker, jenkins, ansible(ansible playbook)



# 진행
1. github maven 프로젝트 개설
2. jenkins container 배포
3. jenkins ci/cd 설정: github 프로젝트 빌드 + host tomcat 베포
4. jenkins build trigger 설정: git - poll SCM
5. jenkins ci/cd 설정: ssh+docker container 안에 tamcat container로 war 배포 자동화
6. ansible (ansible playbook) 서버 구축
   1. github push -> jenkins 서버 (war빌드) -> ansible 서버
   2. playbook1: ansible 서버에서 tomcat image 빌드 및 푸시
   3. playbook2: taomcat 서버의 tomcat image 삭제, tomcat container 중지 및 삭제, tomcat container 재배포
