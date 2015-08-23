## MemberInfo仕様書

### 概要

- クラス名: MemberList
- パッケージ名: jp.ac.oit.igakilab.marsh.smanager


### 説明

LabMemberManagerプロジェクトにおけるメンバーの情報を格納するクラスです。MemberInfoをList型のコレクションに格納し、MemberInfo.getName()などにより、名前の重複がないようにメンバーの情報を管理します。


### フィールド

- インスタンスフィールド
 - **private List<MemberInfo\> list**
 - **private LogRecorder logrec**


### コンストラクタ

- **MemberList()**
- **MemberList(LogRecorder r0)**


### メソッド

- インスタンスメソッド
 - **public void addMemberInfo(MemberInfo mi)**
 - **public void setMemberInfo(MemberInfo mi)**
 - **public void deleteMemberInfo(int idx)**
 - **public MemberInfo getMemberInfo(int idx)**
 
 - **public void deleteMemberInfo(String name)**
 - **public MemberInfo getMemberInfo(String name)**
 
 - **public int searchMemberInfoByName(String name)**
 - **public boolean isMemberInfoRegisted(String name)**

 - **public int getMemberListLength()**
 - **public MemberInfo[] getMemberInfoList()**
 
