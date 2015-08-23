## MemberInfo仕様書

### 概要

- クラス名: MemberInfo
- パッケージ名: jp.ac.oit.igakilab.marsh.smanager


### 説明

LabMemberManagerプロジェクトにおけるメンバーの情報を表現するクラスです。基本的にはget/set用のメソッドとtoString等のメソッドのみからなり、フィールドに各情報を格納します。getNameは必須のメソッドになります。


### フィールド

- インスタンスフィールド
 - **private String name**  
   名前を文字列で格納します。リストなどでのキーにもなります。
 - **private int stateCode**  
   状態を表す整数値を格納します。
 - **private Date loginDate**  
   ログイン日時を格納します。
 - **private Date updateDate**  
   最終更新時間を格納します。


### コンストラクタ

- **public MemberInfo(String n0, int s0, Date d0, Date d1)**  
名前n0,状態コードs0,ログイン日時d0,アップデート日時d1でインスタンスを生成します。
- **public MemberInfo(String n0, int s0, Date d0)**  
名前n0,状態コードs0,ログイン日時d0でインスタンスを生成します。アップデート日時は現在の時間で初期化されます。
- **public MemberInfo(String n0)**  
名前n0でインスタンスを生成します。アップデート日時は現在の時間で初期化され、その他のフィールドは0またはnullで初期化されます。

### メソッド
- インスタンスメソッド
 - **public String getName()**
 - **public void setName(String n0)**
 - **public int getStateCode()**
 - **public void setStateCode(int s0)**
 - **public Date getLoginDate()**
 - **public void setLoginDate(Date d0)**
 - **public Date getUpdateDate()**
 - **public void setUpdateDate(Date d0)**

 - **public void updateDate()**  
   アップデート日時を今の時間に設定します
 - **public boolean updateMemberInfo(MemberInfo mi)**  
   miとの差分をとり、nullになっていないフィールドを適用します。アップデート日時も比較対象になります。自動的にアップデート日時が更新されないので所定のメソッドを実行する必要があります。変更箇所があった場合はtrueが返されます。
 - **public String toString()**  
   インスタンスの情報を出力します。

