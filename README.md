# Online Class API Mock Server

このリポジトリでは、Prism を使用して Online Class API のモックサーバーを起動する方法を説明します。

---

## 📦 **環境の前提条件**

- **Node.js**（必須）
- **npm / yarn**（Node.js に付属）
- **Prism**（API モックサーバーツール）

---

## **🔧 インストール方法**

### 1️⃣ **Prism のインストール**

Prism をグローバルにインストールします。

```bash
npm install -g @stoplight/prism-cli
```

## **🚀 モックサーバーの起動方法**

1️⃣ **Prism を使ってモックサーバーを起動**

```bash
prism mock ./openapi.yaml
```

**成功メッセージの例**:

```
[CLI] ℹ  info      Serving the API on http://127.0.0.1:4010
```

デフォルトでは、**http://localhost:4010** でサーバーが動作します。

> 💡 ポートを変更したい場合は、次のコマンドを使います：
>
> ```bash
> prism mock ./openapi.yaml -p 3000
> ```
>
> これにより、**http://localhost:3000** でサーバーが起動します。

---

## **📡 API リクエストのテスト**

Prism モックサーバーが動作していることを確認するために、**curl**を使ってリクエストを送信してみましょう。

### **GET リクエストの送信**

```bash
curl -X GET http://localhost:4010/v1/user/users/current/learning_course_items
```
