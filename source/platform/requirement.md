## 功能需求描述

### 说明
功能需求分为以下部分：
- 普通用户需求：即不需要与其他功能模块对接，只需要进行数据库操作和前端开发的功能
- 系统功能需求：需要与其他模块对接，调用函数以实现相应请求
- 系统维护需求：即后期维护系统的相关需求，应在开发过程中设计并保留接口，以方便后期功能的新增与更改
- 系统安全需求：关于系统安全和服务的相关需求，包括不仅限于数据库安全，抵御DOS攻击等。
- 系统审计需求：提供界面允许超级用户——系统管理员进行信息的查看，设置的更改等操作。

### 普通用户需求

#### 注册
- 功能：新用户注册平台，允许通过邮箱、手机号两种方式注册平台，并设置用户名，密码。
- 附加需求：
   - 邮箱注册应使用链接确认方法，手机注册应使用短信验证码，并限制链接与验证码的有效时间。
   - 密码不允许出现特殊字符，限制使用 大小写字母，数字，标点符号。
   - 防御DOS攻击的措施：例如1分钟内不可重复发送短信验证码、IP访问限制等。
   - 前端实时正则匹配用户输入的邮箱、手机号、密码的合法性，并显示相应的提示。
   - 后端在得到注册信息后，先进行查重，不允许相同邮箱、手机号、用户名的出现。
- 前置条件：无
- 后置条件：无
- 系统后置行为：
   - 更新用户数据库列表，记录注册时间等相关信息
   - 跳转页面至主页，并将状态置为登录状态，更新用户session信息使浏览器记住密码。
- 异常处理机制：
   - 错误的邮箱、用户名、手机号格式
   - 错误的验证码
   - 验证码、验证链接过期
   - 重复注册的邮箱、手机号、用户名
   - 同一IP短时间内的大量注册请求
- 扩展点：无

#### 登录
- 功能：用户登录网站
- 附加需求：
   - 用户名、密码等的合法性检验
   - 未注册用户名（邮箱，手机号）：提示用户跳转注册页面
   - 多次尝试未正确登录：提示用户找回密码
   - 自动登录功能：在一定时间范围内如果用户已登录过平台，则再次打开平台时直接将状态置为已登录。
- 前置条件：无
- 后置条件：无
- 系统后置行为：
   - 更新数据库中的登录时间，更新session
   - 跳转页面至主页，并将状态置为登录状态
- 异常处理机制：
   - 错误的账号密码
- 扩展点：
   - 找回密码

#### 找回密码
- 功能：用户忘记密码后重新设置密码
- 附加需求：
   - 为验证用户身份，应类似注册行为通过邮箱、手机号进行验证
   - 新密码的双重确认和正则匹配
- 前置条件：无
- 后置条件：无
- 系统后置行为：
   - 更新数据库中的用户密码，清除session中相关信息
   - 跳转页面至登录界面
- 异常处理机制：
   - 未注册的账号
- 扩展点：无

#### 修改个人信息
- 功能：用户忘记密码后重新设置密码
- 附加需求：
   - 为验证用户身份，应类似注册行为通过邮箱、手机号进行验证
   - 新密码的双重确认和正则匹配
- 前置条件：无
- 后置条件：无
- 系统后置行为：
   - 更新数据库中的用户密码，清除session中相关信息
   - 跳转页面至登录界面
- 异常处理机制：
   - 未注册的账号
- 扩展点：无