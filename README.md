# nexus_npm_setting
nodejs nexus 연동 설정


1. nexus repository 설정
   1-1. repository에 npm 관련 host, group, proxy 설정
    (참고 URL : https://lyasee.tistory.com/27)

2. node 설정
   2-1. npm login --registry="1-1에서 설정한 repo URL"
   2-2. nexus 로그인

3. package.json 설정
   3-1. "publishConfig": {
     "registry": "1-1에서 설정한 nexus repo의 URL"  
   }
   중요 : 3-1.의 설정한 URL의 경우 group이 아닌 호스트여야함.
   3-2. npm config ls -l
        -> registry = "3-1.에서 설정한 URL"
         -> 만약 없으면 npm config set registry="3-1에서 설정한 URL"


참고 사이트 : https://devblog.kakaostyle.com/ko/2022-03-07-1-npm-private-repository/
              https://lyasee.tistory.com/27
