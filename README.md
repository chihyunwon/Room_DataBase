# *목표*

안드로이드 Room 라이브러리는 SQLite에 대한 추상화 레이어를 제공하여, SQLite의 모든 기능을 활용하면서도 더 견고하고 편리한 데이터베이스 액세스를 가능하게 하는 라이브러리입니다
앱을 실행하는 기기에서 앱 데이터의 캐시를 만들 수 있으며, 이 캐시는 앱의 단일 정보 소스로서 작동하여 사용자가 인터넷 연결 여부와 관계없이 주요 정보를 볼 수 있게 해줍니다1.

- 데이터베이스 클래스 (Room Database): 데이터베이스를 보유하고 앱의 영구 데이터와의 기본 연결을 위한 접근점 역할을 합니다.
- 데이터 항목 (Entities): 앱 데이터베이스의 테이블을 나타냅니다.
- 데이터 액세스 객체 (DAO): 앱이 데이터베이스의 데이터를 쿼리, 업데이트, 삽입, 삭제하는 데 사용할 수 있는 메서드를 제공합니다.

- SQL 쿼리의 컴파일 시간 확인: SQL 쿼리 오류를 컴파일 시간에 발견할 수 있어 런타임 오류를 줄일 수 있습니다.
- 반복적인 상용구 코드 최소화: 주석을 통한 편의성 제공으로 반복적이고 오류가 발생하기 쉬운 코드를 줄일 수 있습니다.
- 간소화된 데이터베이스 이전 경로: 데이터베이스 버전 관리와 마이그레이션이 용이합니다.

## Room DB 사용간 주의사항
Primitive Type과 Boxed Type만 사용 가능: 일반 객체로 ORM을 수행하면 속도가 느려지고 메모리 낭비가 심해질 수 있습니다. 일반 객체 사용 시 TypeConverter를 통해 변환해야 합니다.
App Inspection을 통한 DB 테이블 확인: 개발 중에는 App Inspection을 사용하여 DB 테이블을 실시간으로 확인할 수 있습니다

안드로이드 개발에 있어서 Room 라이브러리는 데이터 관리를 훨씬 수월하게 만들어주며, MVVM 디자인 패턴과 함께 사용될 때 앱의 아키텍처를 더욱 견고하게 만들어 줍니다
. 실시간 통신과 같은 기능을 구현할 때도 Room은 데이터를 효율적으로 관리하고 사용자에게 빠른 응답을 제공하는 데 도움을 줄 수 있습니다.