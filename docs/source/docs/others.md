## 1.1. Web技术演化

## 1.1.1. 静态页面

Web技术在最初阶段，网站的主要内容是静态的，大多站点托管在ISP上，由文字和图片组成，制作和表现形式也是以表格为主。当时的用户行为也非常简单，基本只是浏览网页。

## 1.1.2. 多媒体阶段

随着技术的不断发展，音频、视频、Flash等多媒体技术诞生了。多媒体的加入使得网页变得更加生动形象，网页上的交互也给用户带来了更好的体验。

## 1.1.3. CGI阶段

渐渐的，多媒体已经不能满足人们的请求，于是CGI（Common Gateway Interface）应运而生。CGI定义了Web服务器与外部应用程序之间的通信接口标准，因此Web服务器可以通过CGI执行外部程序，让外部程序根据Web请求内容生成动态的内容。

在这个时候，各种编程语言如PHP/ASP/JSP也逐渐加入市场，基于这些语言可以实现更加模块化的、功能更强大的应用程序。

## 1.1.4. Ajax

在开始的时候，用户提交整个表单后才能获取结果，用户体验极差。于是Ajax（Asynchronous Javascript And XML）技术逐渐流行起来，它使得应用在不更新整个页面的前提下也可以获得或更新数据。这使得Web应用程序更为迅捷地回应用户动作，并避免了在网络上发送那些没有改变的信息。

## 1.1.5. MVC

随着Web应用开发越来越标准化，出现了MVC等思想。MVC是Model/View/Control的缩写，Model用于封装数据和数据处理方法，视图View是数据的HTML展现，控制器Controller负责响应请求，协调Model和View。

Model，View和Controller的分开，是一种典型的关注点分离的思想，使得代码复用性和组织性更好，Web应用的配置性和灵活性也越来越好。而数据访问也逐渐通过面向对象的方式来替代直接的SQL访问，出现了ORM（Object Relation Mapping）的概念。

除了MVC，类似的设计思想还有MVP，MVVM等。

## 1.1.6. RESTful

在CGI时期，前后端通常是没有做严格区分的，随着解耦和的需求不断增加，前后端的概念开始变得清晰。前端主要指网站前台部分，运行在PC端、移动端等浏览器上展现给用户浏览的网页，由HTML5、CSS3、JavaScript组成。后端主要指网站的逻辑部分，涉及数据的增删改查等。

此时，REST（Representation State Transformation）逐渐成为一种流行的Web架构风格。

REST鼓励基于URL来组织系统功能，充分利用HTTP本身的语义，而不是仅仅将HTTP作为一种远程数据传输协议。一般RESTful有以下的特征：

- 域名和主域名分开
  - api.example.com
  - example.com/api/
- 带有版本控制
  - api.example.com/v1
  - api.example.com/v2
- 使用URL定位资源
  - GET /users 获取所有用户
  - GET /team/:team/users 获取某团队所有用户
  - POST /users 创建用户
  - PATCH/PUT /users 修改某个用户数据
  - DELETE /users 删除某个用户数据
- 用 HTTP 动词描述操作
  - GET 获取资源，单个或多个
  - POST 创建资源
  - PUT/PATCH 更新资源，客户端提供完整的资源数据
  - DELETE 删除资源
- 正确使用状态码
  - 使用状态码提高返回数据的可读性
- 默认使用 JSON 作为数据响应格式
- 有清晰的文档

## 1.1.7. 云服务

随着时间的发展，Web的架构越发复杂，代理服务、负载均衡、数据库分表、异地容灾、缓存、CDN、消息队列、安全防护等技术开始应用，增加了Web开发和运维的复杂度。同时云服务开始逐渐发展，部署环境容器化，各个功能拆成微服务或是Serverless的架构。

### 1.1.7.1. CI/CD

持续集成（CI，Continuous Integration）是让开发人员将工作集成到共享分支中的过程。频繁的集成有助于解决隔离，减少每次提交的大小，以降低合并冲突的可能性。

持续交付（CD，Continuous Deployment）是持续集成的扩展，它将构建从集成测试套件部署到预生产环境。这使得它可以直接在类生产环境中评估每个构建，因此开发人员可以在无需增加任何工作量的情况下，验证bug修复或者测试新特性。

### 1.1.7.2. API网关

API网关是一个服务器，客户端只需要使用简单的访问方式，统一访问API网关，由API网关来代理对后端服务的访问，同时由于服务治理特性统一放到API网关上面，服务治理特性的变更可以做到对客户端透明，一定程度上实现了服务治理等基础特性和业务服务的解耦，服务治理特性的升级也比较容易实现。

## 1.1.8. 参考链接

- [Scaling webapps for newbs](https://arcentry.com/blog/scaling-webapps-for-newbs-and-non-techies/)
- [GitHub 的 Restful HTTP API 设计分解](https://learnku.com/articles/24050)
- [Web技术演化](https://websec.readthedocs.io/zh/latest/basic/history.html)