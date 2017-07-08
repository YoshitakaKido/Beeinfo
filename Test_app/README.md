# Test_app

## Rails5を使ってみる

### 新しいアプリケーションの作成

早速アプリを作ってみる。  
Railsでアプリケーションを作成するには以下のコマンドを打つ。  

    $ rails new アプリ名

今回はTest_appという名前のアプリケーションを作成するので以下のようになる。  

    $ rails new Test_app

するとアプリケーションのひな形となるディレクトリやファイルが作成される。  


### Railsのフォルダ構造

作成されたディレクトリの中身は以下のようになっている。  

```txt
.
├── Gemfile
├── Gemfile.lock
├── README.md
├── Rakefile
├── app
│   ├── assets
│   │   ├── config
│   │   │   └── manifest.js
│   │   ├── images
│   │   ├── javascripts
│   │   │   ├── application.js
│   │   │   ├── cable.js
│   │   │   └── channels
│   │   └── stylesheets
│   │       └── application.css
│   ├── channels
│   │   └── application_cable
│   │       ├── channel.rb
│   │       └── connection.rb
│   ├── controllers
│   │   ├── application_controller.rb
│   │   └── concerns
│   ├── helpers
│   │   └── application_helper.rb
│   ├── jobs
│   │   └── application_job.rb
│   ├── mailers
│   │   └── application_mailer.rb
│   ├── models
│   │   ├── application_record.rb
│   │   └── concerns
│   └── views
│       └── layouts
│           ├── application.html.erb
│           ├── mailer.html.erb
│           └── mailer.text.erb
├── bin
│   ├── bundle
│   ├── rails
│   ├── rake
│   ├── setup
│   ├── spring
│   └── update
├── config
│   ├── application.rb
│   ├── boot.rb
│   ├── cable.yml
│   ├── database.yml
│   ├── environment.rb
│   ├── environments
│   │   ├── development.rb
│   │   ├── production.rb
│   │   └── test.rb
│   ├── initializers
│   │   ├── application_controller_renderer.rb
│   │   ├── assets.rb
│   │   ├── backtrace_silencers.rb
│   │   ├── cookies_serializer.rb
│   │   ├── filter_parameter_logging.rb
│   │   ├── inflections.rb
│   │   ├── mime_types.rb
│   │   ├── new_framework_defaults.rb
│   │   ├── session_store.rb
│   │   └── wrap_parameters.rb
│   ├── locales
│   │   └── en.yml
│   ├── puma.rb
│   ├── routes.rb
│   ├── secrets.yml
│   └── spring.rb
├── config.ru
├── db
│   └── seeds.rb
├── folder_contents.txt
├── lib
│   ├── assets
│   └── tasks
├── log
├── public
│   ├── 404.html
│   ├── 422.html
│   ├── 500.html
│   ├── apple-touch-icon-precomposed.png
│   ├── apple-touch-icon.png
│   ├── favicon.ico
│   └── robots.txt
├── test
│   ├── controllers
│   ├── fixtures
│   │   └── files
│   ├── helpers
│   ├── integration
│   ├── mailers
│   ├── models
│   └── test_helper.rb
├── tmp
│   └── cache
│       └── assets
└── vendor
    └── assets
        ├── javascripts
        └── stylesheets
```

現時点では詳しく説明しないが、上の中身がどういうものなのか簡単に書き記しておく。  

```txt
  - app/     アプリケーションのファイル群
　　  - controllers/  コントローラのファイル群
　　  - models/       モデルのファイル群
　　  - views/        ビューのファイル群
  - config/  設定ファイル群
  - db/      スキーマやマイグレーションのファイル群
  - doc/     アプリケーションについてのドキュメントを配置
  - lib/     共有のコードの配置場所
  - log/     ログファイル群
  - public/  Webから直接アクセス可能なファイルを配置
  - script/  スクリプト群
  - test/    テストコードのファイル群
  - tmp/     一時ファイル群
  - vendor/　 外部のコードを配置
```



