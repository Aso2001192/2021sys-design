```uml
@startuml
opt 未登録
ユーザー->webサーバー:ユーザー登録
webサーバー->DBサーバー:ユーザー登録
DBサーバー->DBサーバー:登録処理
@enduml
```
