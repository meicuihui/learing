修改迁移表
* php artisan make:migration alter_tablename_table --table=tablename
* Schema::table('users', function ($table) { $table->string('title')->default('1')-> change(); }) 
* $table->string('title')->default('1')-> change(); 修改表字段
* $table->string('title')->after("name")->default('1')-> change(); 新增表字段,且新增表字段在name之后
* php artisan migrate

 创建表
* php artisan make:migration create_users_table 
php artisan make:migration create_users_table --create=users
php artisan make:migration add_votes_to_users_table --table=users
create指定表名字 table是否生成新的表

数据的填充
* php artisan make:seeder UsersTableSeeder
* database/seeds 目录下：写代码插入数据
* php artisan db:seed --class=UsersTableSeeder 填充数据
* php artisan migrate:refresh --seed 回滚

重新生成ide hlep代码
* php artisan ide-helper:generate  
发邮件问题
cURL error 60 
解决，证书问题
* [下载证书](https://pan.baidu.com/s/1e-UgJrg-3vtB95tCXKv2IA)
* 放在php\extras\ssl目录下
* 配置到php.ini 'curl.cainfo ="C:\Runing\php\extras\ssl\cacert.pem"'
* 重启服务器

身份证验证
'composer require ofcold/identity-card'

```
  //  返回false 或 Ofcold\IdentityCard\IdentityCard
    $result = Ofcold\IdentityCard\IdentityCard::make('32010619831029081');

    if ( $result === false ) {

        return '您的身份证号码不正确';
    }

    print_r($result->toArray());

```
[https://laravel-china.org/topics/12468/identity-card-number-verification-and-identity-card-information-acquisition-in-mainland-china](https://laravel-china.org/topics/12468/identity-card-number-verification-and-identity-card-information-acquisition-in-mainland-china)

