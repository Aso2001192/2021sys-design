```uml
@startuml
opt 未登録
ユーザー->webサーバー:ユーザー登録
webサーバー->DBサーバー:ユーザー登録
DBサーバー->DBサーバー:登録処理
DBサーバー->webサーバー:認証結果

alt 認証成功
webサーバー->ユーザー:登録メッセージを表示
else 認証失敗
webサーバー->ユーザー:失敗メッセージを表示
end

end

ユーザー->webサーバー:ログイン
webサーバー->DBサーバー:ログイン照会
DBサーバー->DBサーバー:ログイン処理
DBサーバー->webサーバー:認証結果
activate ユーザー

alt
webサーバー->ユーザー:ユーザー名を表示
else
webサーバー->ユーザー:失敗メッセージを表示
end

deactivate ユーザー
@enduml
```
