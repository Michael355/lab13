[![Build Status](https://travis-ci.org/n0k8t/lab10.svg?branch=master)](https://travis-ci.org/n0k8t/lab13)
## Laboratory work XIII

### Задание

Написать программы на **C++** для сериализации и десериализации структуры `Person`.

Структура `Person` определяется следующим образом:

```cpp
struct Email {
  std::string nickname;
  std::string server;
};

struct Person {
  std::string  first_name;
  std::string  last_name;
  Email        email;
  size_t       age;
  std::string  phone;
};
```

### Результат проверки валидности через `JSON Lint`.
```
$jsonlint file.json
{
  "age": 19,
  "email_nickname": "petrov_ivan_98@ya.ru",
  "first_name": "Ivan",
  "last_name": "Petrov",
  "phone": "8(800)555-35-35"
}
```
