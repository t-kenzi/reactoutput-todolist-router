・react-routerの実装手順
プロジェクト雛形（main/App、グローバルスタイル）
Router 骨組み（/todos, /todos/new, /todos/:id, /todos/:id/edit, *）
Templates（AppLayout）を適用し、ナビだけ表示
Context/Reducer の土台（空配列でOK）
Atoms 作成（Button, InputText など最小セット）
Molecules（SearchBox / TodoFormRow）
Organisms（TodoList / TodoListItem / TodoDetailCard）
Pages 実装
/todos：ダミーデータで一覧 → 検索はURLクエリから
/todos/new：フォーム → ADD_TODO → 一覧へ
/todos/:id：詳細表示 → 編集/削除動線
/todos/:id/edit：フォーム → UPDATE_TODO
削除導線（ConfirmDeleteDialog → DELETE_TODO）
永続化（storage モジュールで localStorage 連携）
バリデーション（validators で共通化、フォームに組み込み）
空/エラー/ローディング 表示の整備