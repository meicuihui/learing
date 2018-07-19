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

