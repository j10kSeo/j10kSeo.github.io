

- server2client
- method: graphql-yoga => use PubSub, add Context (new PubSub server)
    - in implementation: pubsub.asyncIterator
    - pubsub.publish 를 이용해서 서버 업데이트가 바로 클라이언트에 전달. 채널을 이용.
        - subscription resolver에서 asyncIterator를 걸고 mutation에서 createComment 등에서 publish하는 형태
     
- Prisma
    - ORM (Object Relational Mapping), Sequelize, Mongoose가 MySQL, MongoDB에 종속적인 반면 Prisma는 그렇지 않음.
    - mutation, subscription을 설정할 필요 없다. type만 생성해도 default로 설정된다.
        - 구현된 mutation이 mongoDB이든 MySQL이든 코드 수정없이 잘 동작한다!
    - node libraries
        - prisma-binding, graphql-cli (for fetching schema, .graphqlconfig)
    - 4466 접속 에러날 때
        - heroku credential이 갱신되었음. 자주 변경되는지, 룰을 살펴봐야 함.