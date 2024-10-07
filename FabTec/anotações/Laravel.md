
=> php artisan serve
=> php artisan make:controller --resource / -r

| Verb      | URI                    | Action  | Route Name     |     |
| --------- | ---------------------- | ------- | -------------- | --- |
| GET       | `/photos`              | index   | photos.index   |     |
| GET       | `/photos/create`       | create  | photos.create  |     |
| POST      | `/photos`              | store   | photos.store   |     |
| GET       | `/photos/{photo}`      | show    | photos.show    |     |
| GET       | `/photos/{photo}/edit` | edit    | photos.edit    |     |
| PUT/PATCH | `/photos/{photo}`      | update  | photos.update  |     |
| DELETE    | `/photos/{photo}`      | destroy | photos.destroy |     |
get pode ser link
delete tem que usar form


=> Route::resources('/aula4', Aula04Controller::class);

=> php artisan make:model Aluno -crm

=> php artisan migration

em Laravel o Model representa uma table no DB;

cada model mapeia diretamente uma tabela. 

php artisan tinker
Psy Shell v0.11.18 (PHP 8.1.2-1ubuntu2.18 — cli) by Justin Hileman
> use App/Models/Aluno

   PARSE ERROR  PHP Parse error: Syntax error, unexpected '/', expecting ';' in vendor/psy/psysh/src/Exception/ParseErrorException.php on line 38.

> use App\Model\Aluno
> $a = new Aluno()

   Error  Class "App\Model\Aluno" not found.

> use App\Models\Aluno
> $a = new Aluno()
= App\Models\Aluno {#7170}

> $a->nome = "Yohanês"
= "Yohanês"

> $a->email ="yzanghelini@gmail.com"
= "yzanghelini@gmail.com"

> $a->save()
= true

> $a
= App\Models\Aluno {#7170
    nome: "Yohanês",
    email: "yzanghelini@gmail.com",
    updated_at: "2024-08-09 16:58:06",
    created_at: "2024-08-09 16:58:06",
    id: 1,
  }

> $alunos = Aluno::all()
= Illuminate\Database\Eloquent\Collection {#7179
    all: [
      App\Models\Aluno {#7185
        id: 1,
        nome: "Yohanês",
        email: "yzanghelini@gmail.com",
        created_at: "2024-08-09 16:58:06",
        updated_at: "2024-08-09 16:58:06",
      },
    ],
  }


criar novo controlador e novas views. Salvando no banco de dados
	use App/Models/Alunos 