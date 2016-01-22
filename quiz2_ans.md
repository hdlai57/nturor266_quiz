1. 請用簡單的方式敘述以下每一行程式碼：

  ```ruby 
  a = 1 
  @a = 2
  @@a = 5
  user = User.new
  user.name
  user.name = "Joe"
  ```
  
#### Ans: 
  ```ruby
  a = 1 # Assign 數字 1 給區域變數 a 
  @a = 2 # Assign 數字 2 給實例變數 a 
  @@ = 5 # Assign 數字 5 給類別變數 a 
  user = User.new # 建立user為User類別的物件
  user.name : 執行User類別裡名為name的method
  user.name = "Joe" # 變更name的實例變數為 String "Joe"
  ```

2. 什麼是 module? 請寫一段程式碼說明一個 class 要如何使用一個 module 裡面的 method?

#### Ans:
  ```
  Module 模組 : 可在模組裡定義方法, 但不像類別Class, 不能用new來建立他
  ```
  ```ruby
  include <module>
  ```

3. 請說明 class variable 和 instance variable 之間的差別

#### Ans:
  ```
  class variable : 可在類別方法跟實例方法使用
  instance variable : 僅可在實例建立後使用

  Refer to:
  可以在實例方法中使用類別變數，不過，你不能在類別方法中使用實例變數，因為類別方法屬於類別擁有，但實例變數屬於實例擁有，類別方法中無法單就 @name 來識別該取得哪個實例的變數值
  ```

4. 請說明 class method 和 instance method 之間的差別

#### Ans:
  ```
  class method: 無需建立物件即可直接使用
  instance method: 僅可在類別建立出之物件使用
  ```

5. 如果今天我為一個叫 User 的 class 產生一個新物件的方式是:
  ```ruby
  User.new("Bob", "male", "Engineer")
  ```
請寫出 User class 的 initialize method

#### Ans:
  ```ruby
  class User
    def initialize(name, gender, job)
      @name = name
      @gender = gender
      @job = job
    end
  end
  ```

6. 在：
  A.  一個 class 裡，method 外面
  B.  一個 class 裡，instance method 裡
  self 分別是指向什麼?

#### Ans:
```
  self 在 method 外面 - 指向物件本身
  self 在 method 裡面 - 指向物件的變數
```
7. attr_accessor 的功能是什麼，它和 attr_reader、attr_writer 之間的差別是什麼？

#### Ans:
```
  attr_accessor: 為可從外部更改實例變數,初始值為nil
  attr_reader: read only
  attr_writer: write only
```

8. 請說明 public 和 private method 之間的不同

#### Ans:
```
  public method 可用物件呼叫
  private mehood 只可在類別內使用
```

9. 請說明 Inheritance 和 Module 之間的差別，它們分別是用於哪些情況？ 請舉例說明

#### Ans:
```
  Inheritance 類別繼承: 子類別能呼叫父類別的方法
  Module 模組: 僅能透過include取得模組裡的方法
```

10. 若今天有一個 class 有 include 一個 module，他的 parent class 和 sub class 是否可以使用該 module 裡的 method?

#### Ans:
```
  Parent class 可以
  Sub class 不可以
```

11. 請間單說明什麼是 Relational Database，什麼是 SQL

#### Ans:
```
  關聯式資料庫：正規化之資料表之間能透過主鍵或外鍵或相關欄位做查詢
  SQL: Structured Query Language (結構化查詢語言) 資料庫管理的程式語言
```
