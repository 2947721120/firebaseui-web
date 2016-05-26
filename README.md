##CN
#<trans data-src="FirebaseUI for Web — Auth" data-dst="firebaseui Web认证" style="background: transparent;">firebaseui Web认证</trans>
<p><trans data-src="FirebaseUI is an open-source JavaScript library for Web that provides simple, customizable UI
bindings on top of " data-dst="firebaseui是Web提供了简单的一个开源的JavaScript库，可定制的用户界面
绑定上" style="background: transparent;">firebaseui是Web提供了简单的一个开源的JavaScript库，可定制的用户界面
绑定上</trans><a href="https://firebase.google.com"><trans data-src="Firebase" data-dst="火力点" style="background: transparent;">火力点</trans></a><trans data-src=" SDKs to eliminate boilerplate code and
promote best practices." data-dst="软件开发工具包消除样板代码和
促进最佳实践。" style="background: transparent;">软件开发工具包消除样板代码和
促进最佳实践。</trans></p>
<p><trans data-src="FirebaseUI Auth provides a drop-in auth solution that handles the UI flows for signing in users with
email addresses and passwords, and Identity Provider Sign In using Google, Facebook and others.
It is built on top of " data-dst="firebaseui认证提供认证解决方案处理UI流
签约用户的电子邮件地址和密码的下降，在使用谷歌身份提供者的标志，脸谱网和其他
它是建立在顶部。" style="background: transparent;">firebaseui认证提供认证解决方案处理UI流
签约用户的电子邮件地址和密码的下降，在使用谷歌身份提供者的标志，脸谱网和其他
它是建立在顶部。</trans></P>
<p><trans data-src="The FirebaseUI component implements best practices for authentication on mobile devices and
websites, helping to sign-in and sign-up conversion for your app. It also handles cases like account
recovery and account linking that can be security sensitive and error-prone to handle." data-dst="的firebaseui组件实现对移动设备和
网站认证的最佳实践，帮助登录和注册你的应用程序的转换。它也处理类似的帐户
回收帐户链接可以安全敏感和容易出错的处理。" style="background: transparent;">的firebaseui组件实现对移动设备和
网站认证的最佳实践，帮助登录和注册你的应用程序的转换。它也处理类似的帐户
回收帐户链接可以安全敏感和容易出错的处理。</trans></p>
<h2><a id="user-content-table-of-contents" class="anchor" href="#table-of-contents" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Table of Contents" data-dst="目录" style="background: transparent;">目录</trans></h2>
<ol>
<li><a href="#installation"><trans data-src="Installation" data-dst="安装">安装</trans></a></li>
<li><a href="#using-firebaseui-for-authentication"><trans data-src="Usage instructions" data-dst="使用说明" style="background: transparent;">使用说明</trans></a></li>
<li><a href="#configuration"><trans data-src="Configuration" data-dst="配置">配置</trans></a></li>
<li><a href="#customizing-firebaseui-for-authentication"><trans data-src="Customization" data-dst="定制">定制</trans></a></li>
<li><a href="#advanced"><trans data-src="Advanced" data-dst="高级">高级</trans></a></li>
</ol>
<h2><a id="user-content-installation" class="anchor" href="#installation" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Installation" data-dst="安装" style="background: transparent;">安装</trans></h2>
<p><trans data-src="You just need to include the following code in the " data-dst="你只需要在如下的代码" style="background: transparent;">你只需要在如下的代码</trans><code><trans data-src="<head>" data-dst="＜head＞">＜head＞</trans></code><trans data-src=" tag of your page:" data-dst="标签页面：">标签页面：</trans></p>
```html
<script src="https://www.gstatic.com/firebasejs/live/3.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/live/3.0/firebase-auth.js"></script>
<script src="https://www.gstatic.com/firebasejs/ui/0.4.0/firebase-ui-auth.js"></script>
<link type="text/css" rel="stylesheet" href="https://www.gstatic.com/firebasejs/ui/0.4.0/firebase-ui-auth.css" />
```
<h2><a id="user-content-using-firebaseui-for-authentication" class="anchor" href="#using-firebaseui-for-authentication" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Using FirebaseUI for Authentication" data-dst="使用firebaseui认证" style="background: transparent;">使用firebaseui认证</trans></h2>
<p><trans data-src="FirebaseUI includes the following flows:" data-dst="firebaseui包括以下流程：" style="background: transparent;">firebaseui包括以下流程：</trans></p>
<ol>
<li><trans data-src="Interaction with Identity Providers such as Google and Facebook" data-dst="与身份提供商如谷歌和脸谱网的相互作用" style="background: transparent;">与身份提供商如谷歌和脸谱网的相互作用</trans></li>
<li><trans data-src="Sign-up and sign-in with email accounts" data-dst="注册和登录的电子邮件帐户">注册和登录的电子邮件帐户</trans></li>
<li><trans data-src="Password reset" data-dst="密码重置">密码重置</trans></li>
<li><trans data-src="Prevention of account duplication (activated when " data-dst="预防帐户重复（激活时" style="background: transparent;">预防帐户重复（激活时</trans><em><trans data-src="" one="" account="" per="" email="" adress""="" data-dst="“一个帐号的电子邮件地址”" style="background: transparent;">“一个帐号的电子邮件地址”</trans></em><trans data-src=" setting is
enabled in the " data-dst="设置中启用
">设置中启用
</trans><a href="https://console.firebase.google.com"><trans data-src="Firebase console" data-dst="Firebase控制台" style="background: transparent;">Firebase控制台</trans></a><trans data-src=". This setting is enabled by
default.)" data-dst="。这个设置是由
默认启用。）" style="background: transparent;">。这个设置是由
默认启用。）</trans></li>
<li><a href="https://www.accountchooser.com/learnmore.html?lang=en"><trans data-src="Account Chooser" data-dst="客户选择">客户选择</trans></a><trans data-src=" for remembering emails" data-dst="记得邮件" style="background: transparent;">记得邮件</trans></li>
</ol>
<h3><a id="user-content-configuring-sign-in-providers" class="anchor" href="#configuring-sign-in-providers" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Configuring sign-in providers" data-dst="在人员配置的标志" style="background: transparent;">在人员配置的标志</trans></h3>
<p><trans data-src="To use FirebaseUI to authenticate users you first need to configure each provider you want to use in
their own developer app settings. Please read the " data-dst="使用firebaseui对用户进行身份验证，您首先需要配置每个供应商要使用在
自己开发的应用程序设置。请阅读" style="background: transparent;">使用firebaseui对用户进行身份验证，您首先需要配置每个供应商要使用在
自己开发的应用程序设置。请阅读</trans><em><trans data-src="Before you begin" data-dst="在你开始之前">在你开始之前</trans></em><trans data-src=" section of Firebase
Authentication at the following links:" data-dst="在下面的链接发
认证部：" style="background: transparent;">在下面的链接发
认证部：</trans></p>
<ul>
<li><a href="https://firebase.google.com/docs/auth/web/password-auth#before_you_begin"><trans data-src="Email and password" data-dst="电子邮件和密码" style="background: transparent;">电子邮件和密码</trans></a></li>
<li><a href="https://firebase.google.com/docs/auth/web/google-signin#before_you_begin"><trans data-src="Google" data-dst="谷歌">谷歌</trans></a></li>
<li><a href="https://firebase.google.com/docs/auth/web/facebook-login#before_you_begin"><trans data-src="Facebook" data-dst="脸书">脸书</trans></a></li>
<li><a href="https://firebase.google.com/docs/auth/web/twitter-login#before_you_begin"><trans data-src="Twitter" data-dst="推特">推特</trans></a></li>
<li><a href="https://firebase.google.com/docs/auth/web/github-auth#before_you_begin"><trans data-src="Github" data-dst="GitHub">GitHub</trans></a></li>
</ul>
<h3><a id="user-content-starting-the-sign-in-flow" class="anchor" href="#starting-the-sign-in-flow" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Starting the sign-in flow" data-dst="在流程开始的标志" style="background: transparent;">在流程开始的标志</trans></h3>
<p><trans data-src="You first need to initialize your
" data-dst="你首先需要初始化" style="background: transparent;">你首先需要初始化</trans><a href="https://firebase.google.com/docs/web/setup#prerequisites"><trans data-src="Firebase app" data-dst="火力点的应用">火力点的应用</trans></a><trans data-src=". The " data-dst="。这个">。这个</trans><code><trans data-src="firebase.auth.Auth" data-dst="firebase.auth.auth" style="background: transparent;">firebase.auth.auth</trans></code><trans data-src="
instance should be passed to the constructor of " data-dst="实例应该传递给构造函数" style="background: transparent;">实例应该传递给构造函数</trans><code><trans data-src="firebaseui.auth.AuthUI" data-dst="firebaseui.auth.authui">firebaseui.auth.authui</trans></code><trans data-src=". You can then call the
" data-dst="。然后你可以调用" style="background: transparent;">。然后你可以调用</trans><code><trans data-src="start" data-dst="开始">开始</trans></code><trans data-src=" method with the CSS selector that determines where to create the widget, and a configuration
object." data-dst="方法使用CSS选择器，决定创建控件，并配置
对象。" style="background: transparent;">方法使用CSS选择器，决定创建控件，并配置
对象。</trans></p>
<p><trans data-src="The following example shows how to set up a sign-in screen with all supported providers." data-dst="下面的示例演示如何设置一个登录屏幕与所有支持的提供者。" style="background: transparent;">下面的示例演示如何设置一个登录屏幕与所有支持的提供者。</trans></p>
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>样本firebaseui APP</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script src="firebase-ui-auth.js"></script>
    <script type="text/javascript">
      // 火力配置。
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      //firebaseui配置。
      var uiConfig = {
        'signInSuccessUrl': '<url-to-redirect-to-on-success>',
        'signInOptions': [
          firebase.auth.GoogleAuthProvider.PROVIDER_ID,
          firebase.auth.FacebookAuthProvider.PROVIDER_ID,
          firebase.auth.TwitterAuthProvider.PROVIDER_ID,
          firebase.auth.GithubAuthProvider.PROVIDER_ID,
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],
        // 服务网址.
        'tosUrl': '<your-tos-url>',
      };

      //使用Firebase初始化firebaseui部件。
      var app = firebase.initializeApp(config);
      var auth = app.auth();
      var ui = new firebaseui.auth.AuthUI(auth);
      // 开始的方法将等到DOM加载。
      ui.start('#firebaseui-auth-container', uiConfig);
    </script>
    <link type="text/css" rel="stylesheet" href="firebase-ui-auth.css" />
  </head>
  <body>
    <!-- 周围的HTML是原封不动的firebaseui。

你的应用程序可以使用空间为品牌，控制和其他自定义.-->
    <h1>欢迎到我的真棒应用程序</h1>
    <div id="firebaseui-auth-container"></div>
  </body>
</html>
```
<p><trans data-src="Here is how you would track the Auth state across all your pages:" data-dst="这里是你如何将所有页面跟踪认证状态：" style="background: transparent;">这里是你如何将所有页面跟踪认证状态：</trans></p>
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Sample FirebaseUI App</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script type="text/javascript">
      //火力配置。
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      // 实例化的火力验证实例。
      var app = firebase.initializeApp(config);
      var auth = app.auth();

      initApp = function() {
        auth.onAuthStateChanged(function(user) {
          if (user) {
            // 用户签名。
            var displayName = user.displayName;
            var email = user.email;
            var emailVerified = user.emailVerified;
            var photoURL = user.photoURL;
            var uid = user.uid;
            var providerData = user.providerData;
            user.getToken().then(function(accessToken) {
              document.getElementById('quickstart-sign-in-status').textContent = 'Signed in';
              document.getElementById('quickstart-sign-in').textContent = '退出';
              document.getElementById('quickstart-account-details').textContent = JSON.stringify({
                displayName: displayName,
                email: email,
                emailVerified: emailVerified,
                photoURL: photoURL,
                uid: uid,
                accessToken: accessToken,
                providerData: providerData
              }, null, '  ');
            });
          } else {
            // User is signed out.
            document.getElementById('quickstart-sign-in-status').textContent = '签出';
            document.getElementById('quickstart-sign-in').textContent = '登录';
            document.getElementById('quickstart-account-details').textContent = 'null';
          }
        }, function(error) {
          console.log(error);
        });
      };

      window.onload = function() {
        initApp()
      };
    </script>
  </head>
  <body>
    <h1>Welcome to My Awesome App</h1>
    <div id="quickstart-sign-in-status"></div>
    <div id="quickstart-sign-in"></div>
    <div id="quickstart-account-details"></div>
  </body>
</html>

```
<h2><a id="user-content-configuration" class="anchor" href="#configuration" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Configuration" data-dst="配置" style="background: transparent;">配置</trans></h2>
<p><trans data-src="FirebaseUI supports the following configuration parameters." data-dst="firebaseui支持以下配置参数。" style="background: transparent;">firebaseui支持以下配置参数。</trans></p>
<table><thead>
<tr>
<th><trans data-src="Name" data-dst="姓名" style="background: transparent;">姓名</trans></th>
<th><trans data-src="Required" data-dst="要求" style="background: transparent;">要求</trans></th>
<th><trans data-src="Default" data-dst="默认">默认</trans></th>
<th><trans data-src="Description" data-dst="描述">描述</trans></th>
</tr>
</thead><tbody>
<tr>
<td><trans data-src="callbacks" data-dst="回调" style="background: transparent;">回调</trans></td>
<td><trans data-src="No" data-dst="否">否</trans></td>
<td><code><trans data-src="[]" data-dst="[]">[]</trans></code></td>
<td><trans data-src="A list of developers " data-dst="一个列表的开发商">一个列表的开发商</trans><a href="#available-callbacks"><trans data-src="callbacks" data-dst="回调">回调</trans></a><trans data-src=" after specific events." data-dst="特定事件发生后。">特定事件发生后。</trans></td>
</tr>
<tr>
<td><trans data-src="queryParameterForSignInSuccessUrl" data-dst="queryparameterforsigninsuccessurl" style="background: transparent;">queryparameterforsigninsuccessurl</trans></td>
<td><trans data-src="No" data-dst="否">否</trans></td>
<td><code><trans data-src="" signinsuccessurl""="" data-dst="“signinsuccessurl”">“signinsuccessurl”</trans></code></td>
<td><trans data-src="The redirect URL parameter name for the sign-in success URL. See " data-dst="重定向的URL参数名为成功的URL标志。看到">重定向的URL参数名为成功的URL标志。看到</trans><a href="#overwriting-the-sign-in-success-url"><trans data-src="Overwriting the sign-in success URL" data-dst="登录成功的URL重写">登录成功的URL重写</trans></a><trans data-src="." data-dst=".">.</trans></td>
</tr>
<tr>
<td><trans data-src="queryParameterForWidgetMode" data-dst="queryparameterforwidgetmode">queryparameterforwidgetmode</trans></td>
<td><trans data-src="No" data-dst="否">否</trans></td>
<td><code><trans data-src="" mode""="" data-dst="“模式”">“模式”</trans></code></td>
<td><trans data-src="The redirect URL parameter name for the “mode” of the Widget. See " data-dst="重定向的URL参数的名称为“模式”的窗口小部件。看到">重定向的URL参数的名称为“模式”的窗口小部件。看到</trans><a href="#firebaseui-widget-modes"><trans data-src="FirebaseUI widget modes" data-dst="firebaseui插件模式">firebaseui插件模式</trans></a><trans data-src="." data-dst=".">.</trans></td>
</tr>
<tr>
<td><trans data-src="signInOptions" data-dst="signinoptions">signinoptions</trans></td>
<td><trans data-src="Yes" data-dst="是的">是的</trans></td>
<td><trans data-src="-" data-dst="-">-</trans></td>
<td><trans data-src="The list of " data-dst="列表">列表</trans><a href="#available-providers"><trans data-src="providers" data-dst="供应商">供应商</trans></a><trans data-src=" enabled for signing into your app. The order you specify them will be the order they are displayed on the sign-in provider selection screen." data-dst="签署为您的应用程序启用。您指定的顺序将它们显示在屏幕上选择供应商签订订单。">签署为您的应用程序启用。您指定的顺序将它们显示在屏幕上选择供应商签订订单。</trans></td>
</tr>
<tr>
<td><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”">“signinsuccessurl”</trans></td>
<td><trans data-src="No" data-dst="否">否</trans></td>
<td><trans data-src="-" data-dst="-">-</trans></td>
<td><trans data-src="The URL where to redirect the user after a successful sign-in. " data-dst="的URL重定向用户成功登录后。">的URL重定向用户成功登录后。</trans><strong><trans data-src="Required" data-dst="要求">要求</trans></strong><trans data-src=" when the " data-dst="当">当</trans><code><trans data-src="signInSuccess" data-dst="signinsuccess">signinsuccess</trans></code><trans data-src=" callback is not used or when it returns " data-dst="回调是不使用或当它返回">回调是不使用或当它返回</trans><code><trans data-src="true" data-dst="真正的">真正的</trans></code><trans data-src="." data-dst=".">.</trans></td>
</tr>
<tr>
<td><trans data-src="tosUrl" data-dst="tosurl">tosurl</trans></td>
<td><trans data-src="Yes" data-dst="是的">是的</trans></td>
<td><trans data-src="-" data-dst="-">-</trans></td>
<td><trans data-src="The URL of the Terms of Service page." data-dst="服务条款的页面的URL。">服务条款的页面的URL。</trans></td>
</tr>
</tbody></table>
<h3><a id="user-content-available-providers" class="anchor" href="#available-providers" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Available providers" data-dst="现有的供应商">现有的供应商</trans></h3>
<table><thead>
<tr>
<th><trans data-src="Provider" data-dst="供应商">供应商</trans></th>
<th><trans data-src="Value" data-dst="价值">价值</trans></th>
</tr>
</thead><tbody>
<tr>
<td><trans data-src="Google" data-dst="谷歌">谷歌</trans></td>
<td><code><trans data-src="firebase.auth.GoogleAuthProvider.PROVIDER_ID" data-dst="firebase.auth.googleauthprovider.provider_id">firebase.auth.googleauthprovider.provider_id</trans></code></td>
</tr>
<tr>
<td><trans data-src="Facebook" data-dst="脸书">脸书</trans></td>
<td><code><trans data-src="firebase.auth.FacebookAuthProvider.PROVIDER_ID" data-dst="firebase.auth.facebookauthprovider.provider_id">firebase.auth.facebookauthprovider.provider_id</trans></code></td>
</tr>
<tr>
<td><trans data-src="Twitter" data-dst="推特">推特</trans></td>
<td><code><trans data-src="firebase.auth.TwitterAuthProvider.PROVIDER_ID" data-dst="firebase.auth.twitterauthprovider.provider_id">firebase.auth.twitterauthprovider.provider_id</trans></code></td>
</tr>
<tr>
<td><trans data-src="Github" data-dst="GitHub">GitHub</trans></td>
<td><code><trans data-src="firebase.auth.GithubAuthProvider.PROVIDER_ID" data-dst="firebase.auth.githubauthprovider.provider_id">firebase.auth.githubauthprovider.provider_id</trans></code></td>
</tr>
<tr>
<td><trans data-src="Email and password" data-dst="电子邮件和密码">电子邮件和密码</trans></td>
<td><code><trans data-src="firebase.auth.EmailAuthProvider.PROVIDER_ID" data-dst="firebase.auth.emailauthprovider.provider _ ID">firebase.auth.emailauthprovider.provider _ ID</trans></code></td>
</tr>
</tbody></table>
<h3><a id="user-content-available-callbacks" class="anchor" href="#available-callbacks" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Available callbacks" data-dst="可回调">可回调</trans></h3>
<p><trans data-src="Currently only one callback is supported. Some will be added soon to monitor UI changes." data-dst="目前只有一个回调的支持。有些会很快加入到监控界面的变化。" style="background: transparent;">目前只有一个回调的支持。有些会很快加入到监控界面的变化。</trans></p>
`signInSuccess(currentUser, credential, redirectUrl)`
<p><strong><trans data-src="Parameters:" data-dst="参数：" style="background: transparent;">参数：</trans></strong></p>
<table><thead>
<tr>
<th><trans data-src="Name" data-dst="名称" style="background: transparent;">名称</trans></th>
<th><trans data-src="Type" data-dst="类型" style="background: transparent;">类型</trans></th>
<th><trans data-src="Optional" data-dst="可选" style="background: transparent;">可选</trans></th>
<th><trans data-src="Description" data-dst="描述">描述</trans></th>
</tr>
</thead><tbody>
<tr>
<td><code><trans data-src="currentUser" data-dst="currentUser" style="background: transparent;">currentUser</trans></code></td>
<td><code><trans data-src="firebase.User" data-dst="firebase.User" style="background: transparent;">firebase.User</trans></code></td>
<td><trans data-src="No" data-dst="否">否</trans></td>
<td><trans data-src="The logged in user." data-dst="登录用户。" style="background: transparent;">登录用户。</trans></td>
</tr>
<tr>
<td><code><trans data-src="credential" data-dst="credential">credential</trans></code></td>
<td><code><trans data-src="firebase.auth.AuthCredential" data-dst="firebase.auth.authcredential" style="background: transparent;">firebase.auth.authcredential</trans></code></td>
<td><trans data-src="Yes" data-dst="是的">是的</trans></td>
<td><trans data-src="he credential used to sign in the user." data-dst="他凭据用于登录的用户。">他凭据用于登录的用户。</trans></td>
</tr>
<tr>
<td><code><trans data-src="redirectUrl" data-dst="redirecturl">redirecturl</trans></code></td>
<td><code><trans data-src="string" data-dst="字符串">字符串</trans></code></td>
<td><trans data-src="Yes" data-dst="是的">是的</trans></td>
<td><trans data-src="The URL where the user is redirected after the callback finishes. It will only be given if you " data-dst="URL，用户被重定向回调结束后。它只会给你" style="background: transparent;">URL，用户被重定向回调结束后。它只会给你</trans><a href="#overwriting-the-sign-in-success-url"><trans data-src="overwrite the sign-in success URL" data-dst="覆盖在成功URL的标志">覆盖在成功URL的标志</trans></a><trans data-src="." data-dst=".">.</trans></td>
</tr>
</tbody></table>
<p><strong><trans data-src="Should return: " data-dst="应该返回：" style="background: transparent;">应该返回：</trans><code><trans data-src="boolean" data-dst="布尔" style="background: transparent;">布尔</trans></code></strong></p>
<p><trans data-src="If the callback returns " data-dst="如果回调函数返回" style="background: transparent;">如果回调函数返回</trans><code><trans data-src="true" data-dst="真正的">真正的</trans></code><trans data-src=", then the page is automatically redirected depending on the case:" data-dst="，然后页面自动重定向根据情况：">，然后页面自动重定向根据情况：</trans></p>
<ul>
<li><trans data-src="If no " data-dst="如果没有" style="background: transparent;">如果没有</trans><code><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”" style="background: transparent;">“signinsuccessurl”</trans></code><trans data-src=" parameter was given in the URL (See:
" data-dst="参数是在给出的URL（见：" style="background: transparent;">参数是在给出的URL（见：</trans><a href="#overwriting-the-sign-in-success-url"><trans data-src="Overwriting the sign-in success URL" data-dst="登录成功的URL重写">登录成功的URL重写</trans></a><trans data-src=") then the default
" data-dst="）然后默认">）然后默认</trans><code><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”">“signinsuccessurl”</trans></code><trans data-src=" in config is used." data-dst="在配置使用。" style="background: transparent;">在配置使用。</trans></li>
<li><trans data-src="If the value is provided in the URL, that value will be used instead of the static
" data-dst="如果该值是在提供的网址，这个值将被用来代替静态" style="background: transparent;">如果该值是在提供的网址，这个值将被用来代替静态</trans><code><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”" style="background: transparent;">“signinsuccessurl”</trans></code><trans data-src=" in config." data-dst="在配置。">在配置。</trans></li>
</ul>
<p><trans data-src="If the callback returns " data-dst="如果回调函数返回" style="background: transparent;">如果回调函数返回</trans><code><trans data-src="false" data-dst="假">假</trans></code><trans data-src=" or nothing, the page is not automatically redirected." data-dst="或者什么都没有，网页是不会自动重定向。">或者什么都没有，网页是不会自动重定向。</trans></p>
<h3><a id="user-content-example-with-all-parameters-used" class="anchor" href="#example-with-all-parameters-used" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Example with all parameters used" data-dst="所有参数的例子" style="background: transparent;">所有参数的例子</trans></h3>
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Sample FirebaseUI App</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script src="firebase-ui-auth.js"></script>
    <script type="text/javascript">
      // Firebase config.
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      // FirebaseUI config.
      var uiConfig = {
        // Query parameter name for mode.
        'queryParameterForWidgetMode': 'mode',
        // Query parameter name for sign in success url.
        'queryParameterForSignInSuccessUrl': 'signInSuccessUrl',
        'signInSuccessUrl': '<url-to-redirect-to-on-success>',
        'signInOptions': [
          firebase.auth.GoogleAuthProvider.PROVIDER_ID,
          firebase.auth.FacebookAuthProvider.PROVIDER_ID,
          firebase.auth.TwitterAuthProvider.PROVIDER_ID,
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],
        // Terms of service url.
        'tosUrl': '<your-tos-url>',
        'callbacks': {
          'signInSuccess': function(currentUser, credential, redirectUrl) {
            // Do something.
            // Return type determines whether we continue the redirect automatically
            // or whether we leave that to developer to handle.
            return true;
          }
        }
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var app = firebase.initializeApp(config);
      var auth = app.auth();
      var ui = new firebaseui.auth.AuthUI(auth);
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);
    </script>
    <link type="text/css" rel="stylesheet" href="firebase-ui-auth.css" />
  </head>
  <body>
    <!-- The surrounding HTML is left untouched by FirebaseUI.
         Your app may use that space for branding, controls and other customizations.-->
    <h1>Welcome to My Awesome App</h1>
    <div id="firebaseui-auth-container"></div>
  </body>
</html>
```

<h2><a id="user-content-customizing-firebaseui-for-authentication" class="anchor" href="#customizing-firebaseui-for-authentication" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Customizing FirebaseUI for authentication" data-dst="定制firebaseui认证" style="background: transparent;">定制firebaseui认证</trans></h2>
<p><trans data-src="Currently, FirebaseUI does not offer customization out of the box. However, the HTML around the
widget is not affected by it so you can display everything you want around the widget container." data-dst="目前，firebaseui不提供定制的盒子。然而，在
控件的HTML并不受它的影响，你可以显示你想要的控件容器周围的一切。" style="background: transparent;">目前，firebaseui不提供定制的盒子。然而，在
控件的HTML并不受它的影响，你可以显示你想要的控件容器周围的一切。</trans></p>
<h2><a id="user-content-advanced" class="anchor" href="#advanced" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Advanced" data-dst="高级" style="background: transparent;">高级</trans></h2>

<h3><a id="user-content-firebaseui-widget-modes" class="anchor" href="#firebaseui-widget-modes" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="FirebaseUI widget modes" data-dst="firebaseui插件模式" style="background: transparent;">firebaseui插件模式</trans></h3>
<p><trans data-src="Upon initilization, FirebaseUI will look for the " data-dst="在实例上，firebaseui会找" style="background: transparent;">在实例上，firebaseui会找</trans><code><trans data-src="mode" data-dst="“mode”" style="background: transparent;">“mode”</trans></code><trans data-src=" parameter in the URL. Depending on the value
of this parameter, it will trigger a specific mode. When no " data-dst="URL中的参数。根据这个参数的值
，它会触发一个特定的模式。当没有" style="background: transparent;">URL中的参数。根据这个参数的值
，它会触发一个特定的模式。当没有</trans><code><trans data-src="mode" data-dst="“mode”">“mode”</trans></code><trans data-src=" parameter is found, it will
default to the sign-in mode." data-dst="参数，它将
默认模式的标志。" style="background: transparent;">参数，它将
默认模式的标志。</trans></p>
<p><trans data-src="You can change the name of this parameter with the " data-dst="你可以用改变此参数的名称" style="background: transparent;">你可以用改变此参数的名称</trans><code><trans data-src="queryParameterForWidgetMode" data-dst="queryparameterforwidgetmode">queryparameterforwidgetmode</trans></code><trans data-src=" configuration
parameter." data-dst="
参数配置。">
参数配置。</trans></p>
<table><thead>
<tr>
<th><trans data-src="Query parameter value" data-dst="查询参数的值" style="background: transparent;">查询参数的值</trans></th>
<th><trans data-src="Description" data-dst="描述"><trans data-src="描述" data-dst="描述" style="background: transparent;">描述</trans></trans></th>
</tr>
</thead><tbody>
<tr>
<td><code>?mode=select</code></td>
<td><trans data-src="Sign-in mode" data-dst="登录模式">登录模式</trans></td>
</tr>
</tbody></table>
<p><strong><trans data-src="Example:" data-dst="例子：">例子：</trans></strong></p>
**Example:**

    https://<url-of-the-widget>?mode=select
<h3><a id="user-content-overwriting-the-sign-in-success-url" class="anchor" href="#overwriting-the-sign-in-success-url" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Overwriting the sign-in success URL" data-dst="登录成功的URL重写" style="background: transparent;">登录成功的URL重写</trans></h3>
<p><trans data-src="You can pass a query parameter to the widget's URL that will overwrite the URL the user is
redirected to after a successful sign-in. If you do so, you must set the configuration
" data-dst="你可以通过查询参数的小工具的URL的URL将覆盖用户
重定向到一个成功登录后。如果你这样做，你必须设置配置" style="background: transparent;">你可以通过查询参数的小工具的URL的URL将覆盖用户
重定向到一个成功登录后。如果你这样做，你必须设置配置</trans><code><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”" style="background: transparent;">“signinsuccessurl”</trans></code><trans data-src=" value (even if it will be overwritten). When passing the redirect URL this way,
the " data-dst="价值（即使它将被覆盖）。当通过重定向URL，这样，
">价值（即使它将被覆盖）。当通过重定向URL，这样，
</trans><code><trans data-src="signInSuccess" data-dst="signinsuccess">signinsuccess</trans></code><trans data-src=" callback will receive the value as the " data-dst="回调将获得价值为" style="background: transparent;">回调将获得价值为</trans><code><trans data-src="redirectUrl" data-dst="redirecturl" style="background: transparent;">redirecturl</trans></code><trans data-src=" argument." data-dst="争论。">争论。</trans></p>
<p><trans data-src="You " data-dst="你">你</trans><strong><trans data-src="must include the mode explicitly" data-dst="必须包括明确的模式">必须包括明确的模式</trans></strong><trans data-src=" in the URL when using the " data-dst="在URL中使用时">在URL中使用时</trans><code><trans data-src="signInSuccessUrl" data-dst="“signinsuccessurl”">“signinsuccessurl”</trans></code><trans data-src=" parameter,
otherwise FirebaseUI will directly redirect to the URL specified." data-dst="
参数，否则firebaseui直接重定向URL的。">
参数，否则firebaseui直接重定向URL的。</trans></p>
<p><trans data-src="You can change the name of this parameter with the " data-dst="你可以用改变此参数的名称" style="background: transparent;">你可以用改变此参数的名称</trans><code><trans data-src="queryParameterForSignInSuccessUrl" data-dst="queryparameterforsigninsuccessurl" style="background: transparent;">queryparameterforsigninsuccessurl</trans></code><trans data-src=" configuration
parameter." data-dst="
参数配置。">
参数配置。</trans></p>
<p><strong><trans data-src="Example:" data-dst="例子：">例子：</trans></strong></p>
**Example:**

`https://<url-of-the-widget>?mode=select&signInSuccessUrl=signedIn.html` 将用户重定向到
`https://<url-of-the-widget>/signedIn.html` 在一个成功的迹象在流。

##EN
# FirebaseUI for Web — Auth

FirebaseUI is an open-source JavaScript library for Web that provides simple, customizable UI
bindings on top of [Firebase](https://firebase.google.com) SDKs to eliminate boilerplate code and
promote best practices.

FirebaseUI Auth provides a drop-in auth solution that handles the UI flows for signing in users with
email addresses and passwords, and Identity Provider Sign In using Google, Facebook and others.
It is built on top of [Firebase Auth](https://firebase.google.com/docs/auth).

The FirebaseUI component implements best practices for authentication on mobile devices and
websites, helping to sign-in and sign-up conversion for your app. It also handles cases like account
recovery and account linking that can be security sensitive and error-prone to handle.

FirebaseUI Auth clients are also available for [iOS](https://github.com/firebase/firebaseui-ios) and
[Android](https://github.com/firebase/firebaseui-android).

## Table of Contents

1. [Installation](#installation)
2. [Usage instructions](#using-firebaseui-for-authentication)
3. [Configuration](#configuration)
4. [Customization](#customizing-firebaseui-for-authentication)
5. [Advanced](#advanced)

## Installation

You just need to include the following code in the `<head>` tag of your page:

```html
<script src="https://www.gstatic.com/firebasejs/live/3.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/live/3.0/firebase-auth.js"></script>
<script src="https://www.gstatic.com/firebasejs/ui/0.4.0/firebase-ui-auth.js"></script>
<link type="text/css" rel="stylesheet" href="https://www.gstatic.com/firebasejs/ui/0.4.0/firebase-ui-auth.css" />
```

## Using FirebaseUI for Authentication

FirebaseUI includes the following flows:

1. Interaction with Identity Providers such as Google and Facebook
2. Sign-up and sign-in with email accounts
3. Password reset
4. Prevention of account duplication (activated when *"One account per email adress"* setting is
enabled in the [Firebase console](https://console.firebase.google.com). This setting is enabled by
default.)
5. [Account Chooser](https://www.accountchooser.com/learnmore.html?lang=en) for remembering emails

### Configuring sign-in providers

To use FirebaseUI to authenticate users you first need to configure each provider you want to use in
their own developer app settings. Please read the *Before you begin* section of Firebase
Authentication at the following links:

- [Email and password](https://firebase.google.com/docs/auth/web/password-auth#before_you_begin)
- [Google](https://firebase.google.com/docs/auth/web/google-signin#before_you_begin)
- [Facebook](https://firebase.google.com/docs/auth/web/facebook-login#before_you_begin)
- [Twitter](https://firebase.google.com/docs/auth/web/twitter-login#before_you_begin)
- [Github](https://firebase.google.com/docs/auth/web/github-auth#before_you_begin)

### Starting the sign-in flow

You first need to initialize your
[Firebase app](https://firebase.google.com/docs/web/setup#prerequisites). The `firebase.auth.Auth`
instance should be passed to the constructor of `firebaseui.auth.AuthUI`. You can then call the
`start` method with the CSS selector that determines where to create the widget, and a configuration
object.

The following example shows how to set up a sign-in screen with all supported providers.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Sample FirebaseUI App</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script src="firebase-ui-auth.js"></script>
    <script type="text/javascript">
      // Firebase config.
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      // FirebaseUI config.
      var uiConfig = {
        'signInSuccessUrl': '<url-to-redirect-to-on-success>',
        'signInOptions': [
          firebase.auth.GoogleAuthProvider.PROVIDER_ID,
          firebase.auth.FacebookAuthProvider.PROVIDER_ID,
          firebase.auth.TwitterAuthProvider.PROVIDER_ID,
          firebase.auth.GithubAuthProvider.PROVIDER_ID,
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],
        // Terms of service url.
        'tosUrl': '<your-tos-url>',
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var app = firebase.initializeApp(config);
      var auth = app.auth();
      var ui = new firebaseui.auth.AuthUI(auth);
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);
    </script>
    <link type="text/css" rel="stylesheet" href="firebase-ui-auth.css" />
  </head>
  <body>
    <!-- The surrounding HTML is left untouched by FirebaseUI.
         Your app may use that space for branding, controls and other customizations.-->
    <h1>Welcome to My Awesome App</h1>
    <div id="firebaseui-auth-container"></div>
  </body>
</html>
```

Here is how you would track the Auth state across all your pages:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Sample FirebaseUI App</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script type="text/javascript">
      // Firebase config.
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      // Instantiates the Firebase Auth instance.
      var app = firebase.initializeApp(config);
      var auth = app.auth();

      initApp = function() {
        auth.onAuthStateChanged(function(user) {
          if (user) {
            // User is signed in.
            var displayName = user.displayName;
            var email = user.email;
            var emailVerified = user.emailVerified;
            var photoURL = user.photoURL;
            var uid = user.uid;
            var providerData = user.providerData;
            user.getToken().then(function(accessToken) {
              document.getElementById('quickstart-sign-in-status').textContent = 'Signed in';
              document.getElementById('quickstart-sign-in').textContent = 'Sign out';
              document.getElementById('quickstart-account-details').textContent = JSON.stringify({
                displayName: displayName,
                email: email,
                emailVerified: emailVerified,
                photoURL: photoURL,
                uid: uid,
                accessToken: accessToken,
                providerData: providerData
              }, null, '  ');
            });
          } else {
            // User is signed out.
            document.getElementById('quickstart-sign-in-status').textContent = 'Signed out';
            document.getElementById('quickstart-sign-in').textContent = 'Sign in';
            document.getElementById('quickstart-account-details').textContent = 'null';
          }
        }, function(error) {
          console.log(error);
        });
      };

      window.onload = function() {
        initApp()
      };
    </script>
  </head>
  <body>
    <h1>Welcome to My Awesome App</h1>
    <div id="quickstart-sign-in-status"></div>
    <div id="quickstart-sign-in"></div>
    <div id="quickstart-account-details"></div>
  </body>
</html>

```

## Configuration

FirebaseUI supports the following configuration parameters.

|Name                             |Required|Default             |Description                                                                                                                                                                               |
|---------------------------------|--------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|callbacks                        |No      |`[]`                |A list of developers [callbacks](#available-callbacks) after specific events.                                                                                                             |
|queryParameterForSignInSuccessUrl|No      |`"signInSuccessUrl"`|The redirect URL parameter name for the sign-in success URL. See [Overwriting the sign-in success URL](#overwriting-the-sign-in-success-url).                                             |
|queryParameterForWidgetMode      |No      |`"mode"`            |The redirect URL parameter name for the “mode” of the Widget. See [FirebaseUI widget modes](#firebaseui-widget-modes).                                                                    |
|signInOptions                    |Yes     |-                   |The list of [providers](#available-providers) enabled for signing into your app. The order you specify them will be the order they are displayed on the sign-in provider selection screen.|
|signInSuccessUrl                 |No      |-                   |The URL where to redirect the user after a successful sign-in. **Required** when the `signInSuccess` callback is not used or when it returns `true`.                                      |
|tosUrl                           |Yes     |-                   |The URL of the Terms of Service page.                                                                                                                                                     |

### Available providers

|Provider          |Value                                           |
|------------------|------------------------------------------------|
|Google            |`firebase.auth.GoogleAuthProvider.PROVIDER_ID`  |
|Facebook          |`firebase.auth.FacebookAuthProvider.PROVIDER_ID`|
|Twitter           |`firebase.auth.TwitterAuthProvider.PROVIDER_ID` |
|Github            |`firebase.auth.GithubAuthProvider.PROVIDER_ID`  |
|Email and password|`firebase.auth.EmailAuthProvider.PROVIDER_ID`   |

### Available callbacks

Currently only one callback is supported. Some will be added soon to monitor UI changes.

`signInSuccess(currentUser, credential, redirectUrl)`

**Parameters:**

|Name         |Type                          | Optional|Description                                                                                                                                                              |
|-------------|------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`currentUser`|`firebase.User`               |No       |The logged in user.                                                                                                                                                      |
|`credential` |`firebase.auth.AuthCredential`|Yes      |he credential used to sign in the user.                                                                                                                                  |
|`redirectUrl`|`string`                      |Yes      |The URL where the user is redirected after the callback finishes. It will only be given if you [overwrite the sign-in success URL](#overwriting-the-sign-in-success-url).|

**Should return: `boolean`**

If the callback returns `true`, then the page is automatically redirected depending on the case:

- If no `signInSuccessUrl` parameter was given in the URL (See:
[Overwriting the sign-in success URL](#overwriting-the-sign-in-success-url)) then the default
`signInSuccessUrl` in config is used.
- If the value is provided in the URL, that value will be used instead of the static
`signInSuccessUrl` in config.

If the callback returns `false` or nothing, the page is not automatically redirected.


### Example with all parameters used

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Sample FirebaseUI App</title>
    <script src="firebase-app.js"></script>
    <script src="firebase-auth.js"></script>
    <script src="firebase-ui-auth.js"></script>
    <script type="text/javascript">
      // Firebase config.
      var config = {
        'authDomain': '<your-firebase-project-domain>.firebaseapp.com',
        'apiKey': '<your-API-key>',
      };

      // FirebaseUI config.
      var uiConfig = {
        // Query parameter name for mode.
        'queryParameterForWidgetMode': 'mode',
        // Query parameter name for sign in success url.
        'queryParameterForSignInSuccessUrl': 'signInSuccessUrl',
        'signInSuccessUrl': '<url-to-redirect-to-on-success>',
        'signInOptions': [
          firebase.auth.GoogleAuthProvider.PROVIDER_ID,
          firebase.auth.FacebookAuthProvider.PROVIDER_ID,
          firebase.auth.TwitterAuthProvider.PROVIDER_ID,
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],
        // Terms of service url.
        'tosUrl': '<your-tos-url>',
        'callbacks': {
          'signInSuccess': function(currentUser, credential, redirectUrl) {
            // Do something.
            // Return type determines whether we continue the redirect automatically
            // or whether we leave that to developer to handle.
            return true;
          }
        }
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var app = firebase.initializeApp(config);
      var auth = app.auth();
      var ui = new firebaseui.auth.AuthUI(auth);
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);
    </script>
    <link type="text/css" rel="stylesheet" href="firebase-ui-auth.css" />
  </head>
  <body>
    <!-- The surrounding HTML is left untouched by FirebaseUI.
         Your app may use that space for branding, controls and other customizations.-->
    <h1>Welcome to My Awesome App</h1>
    <div id="firebaseui-auth-container"></div>
  </body>
</html>
```

## Customizing FirebaseUI for authentication

Currently, FirebaseUI does not offer customization out of the box. However, the HTML around the
widget is not affected by it so you can display everything you want around the widget container.

## Advanced

### FirebaseUI widget modes

Upon initilization, FirebaseUI will look for the `mode` parameter in the URL. Depending on the value
of this parameter, it will trigger a specific mode. When no `mode` parameter is found, it will
default to the sign-in mode.

You can change the name of this parameter with the `queryParameterForWidgetMode` configuration
parameter.

|Query parameter value|Description |
|---------------------|------------|
|`?mode=select`       |Sign-in mode|

**Example:**

    https://<url-of-the-widget>?mode=select

### Overwriting the sign-in success URL

You can pass a query parameter to the widget's URL that will overwrite the URL the user is
redirected to after a successful sign-in. If you do so, you must set the configuration
`signInSuccessUrl` value (even if it will be overwritten). When passing the redirect URL this way,
the `signInSuccess` callback will receive the value as the `redirectUrl` argument.

You **must include the mode explicitly** in the URL when using the `signInSuccessUrl` parameter,
otherwise FirebaseUI will directly redirect to the URL specified.

You can change the name of this parameter with the `queryParameterForSignInSuccessUrl` configuration
parameter.

**Example:**

`https://<url-of-the-widget>?mode=select&signInSuccessUrl=signedIn.html` will redirect the user to
`https://<url-of-the-widget>/signedIn.html` after a successful sign-in flow.
