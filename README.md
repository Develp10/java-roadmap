# ☕ Java Roadmap & Практический курс 2026 — от новичка до Senior

> **Полный путь в Java:** роадмап (карта движения) **+** подробный практический курс с уроками, рабочими примерами кода, разбором ошибок и заданиями.

Этот репозиторий состоит из двух частей:

1. **🗺️ Roadmap** — *что и в каком порядке учить.* Общая карта от нуля до прода.
2. **📘 Практический курс** — *как именно учить.* Готовые уроки с кодом, под каждый уровень роадмапа.

> **Как пользоваться:** иди сверху вниз, не прыгай через уровни. На каждом этапе пиши код руками — без практики теория быстро забывается. Цикл: **теория → пример → свой код → задание → пет-проект.**

---

## 📊 Как устроен путь

```
Новичок → Junior → Middle → Senior
   |          |          |          |
Ур. 0–1    Ур. 2–4    Ур. 5–8    Ур. 9
```

| Этап | Уровни | Ориентировочное время |
|------|--------|----------------------|
| Основы | 0–1 | 1–2 месяца |
| Junior | 2–4 | 3–5 месяцев |
| Middle | 5–8 | 6–12 месяцев |
| Senior | 9 | постоянно |

---

## 🗺️ Содержание

### Часть I. Roadmap
1. [Уровень 0. Подготовка и инструменты](#уровень-0-подготовка-и-инструменты)
2. [Уровень 1. Основы языка (Core Java)](#уровень-1-основы-языка-core-java)
3. [Уровень 2. ООП](#уровень-2-ооп)
4. [Уровень 3. Коллекции и Generics](#уровень-3-коллекции-и-generics)
5. [Уровень 4. Исключения, IO, функциональный стиль](#уровень-4-исключения-io-функциональный-стиль)
6. [Уровень 5. Многопоточность и JVM](#уровень-5-многопоточность-и-jvm)
7. [Уровень 6. Базы данных и SQL](#уровень-6-базы-данных-и-sql)
8. [Уровень 7. Сборка, тесты, Git](#уровень-7-сборка-тесты-git)
9. [Уровень 8. Spring / Spring Boot](#уровень-8-spring--spring-boot)
10. [Уровень 9. Backend в проде](#уровень-9-backend-в-проде-продвинутый)

### Часть II. Практический курс
- [📘 Практический курс по Java](#-практический-курс-по-java)

### Часть III. Дополнительно
- [🚀 Pet-проекты по уровням](#-pet-проекты-по-уровням)
- [📚 Полезные ресурсы](#-полезные-ресурсы)
- [✅ Чек-лист к Junior-собеседованию](#-чек-лист-готовности-к-junior-собеседованию)

---

# Часть I. ROADMAP

## Уровень 0. Подготовка и инструменты

**Цель:** настроить окружение и запустить первый код.

**Теория:**
- Что такое JDK, JRE, JVM и чем они отличаются.
- Как Java компилируется: `.java` → `javac` → байткод `.class` → JVM.
- Версии Java: учим на **LTS** (Java 17 или 21).

**Инструменты:**
- JDK 21 (LTS) — Temurin/Adoptium или Oracle.
- IDE: **IntelliJ IDEA Community** (рекомендуется).
- Git + аккаунт на GitHub.

**Практика:** запусти Hello World из IDE и из терминала (`javac Main.java && java Main`).

> 📘 Подробный разбор — в [Уроке 1 практического курса](#урок-1--первая-программа-и-как-работает-java).

---

## Уровень 1. Основы языка (Core Java)

**Цель:** уверенно писать процедурный код.

**Теория:**
- Примитивные типы (`int`, `long`, `double`, `boolean`, `char`) и обёртки.
- Переменные, `final`, области видимости; операторы, приведение типов.
- Условия: `if/else`, `switch` (вкл. switch-expression).
- Циклы: `for`, `while`, `do-while`, `for-each`.
- Массивы (одно- и многомерные).
- Методы, перегрузка, `varargs`.
- `String`, `StringBuilder`, форматирование.

**Практика:** FizzBuzz · консольный калькулятор · реверс строки и палиндром · min/max и сумма в массиве.

> 📘 [Уроки 1–3 практического курса](#-практический-курс-по-java).

---

## Уровень 2. ООП

**Цель:** мыслить объектами, а не функциями.

**Теория:**
- Класс и объект, поля и методы, конструкторы.
- 4 принципа: инкапсуляция, наследование, полиморфизм, абстракция.
- `this`, `super`, модификаторы доступа; `static`, `final`.
- Абстрактные классы vs интерфейсы (`default`-методы).
- `equals()` / `hashCode()` / `toString()` — контракты.
- `enum`, `record` (Java 16+); композиция против наследования.

**Практика:** иерархия `Shape` → `Circle`/`Rectangle` · модель `Bank` с переводами · `equals/hashCode` руками.

> 📘 [Уроки 4–5 практического курса](#-практический-курс-по-java).

---

## Уровень 3. Коллекции и Generics

**Цель:** выбирать правильную структуру данных.

**Теория:**
- Иерархия: `Collection`, `List`, `Set`, `Queue`, `Map`.
- `ArrayList` vs `LinkedList`, `HashSet` vs `TreeSet`.
- `HashMap` внутри: бакеты, хеши, коллизии.
- Generics: `<T>`, wildcards `? extends` / `? super`.
- `Comparable` vs `Comparator`; `Iterator`, `Iterable`.

**Практика:** частотный словарь · сортировка по нескольким полям · свой `Stack<T>`.

> 📘 [Урок 6 практического курса](#-практический-курс-по-java).

---

## Уровень 4. Исключения, IO, функциональный стиль

**Цель:** надёжный код и современный синтаксис.

**Теория:**
- `checked` vs `unchecked`, `try/catch/finally`, `try-with-resources`, свои исключения.
- File IO: `Files`, `Path`, чтение/запись.
- Лямбды, функциональные интерфейсы (`Function`, `Predicate`, `Supplier`, `Consumer`).
- Stream API: `map`, `filter`, `reduce`, `collect`, `Collectors`; `Optional`.

**Практика:** чтение CSV + агрегация · фильтр/группировка/сортировка пользователей.

> 📘 [Уроки 7–8 практического курса](#-практический-курс-по-java).

---

## Уровень 5. Многопоточность и JVM

**Цель:** понимать, как код исполняется и как работать параллельно.

**Теория:**
- Процессы и потоки, `Thread`, `Runnable`, `Callable`.
- `synchronized`, `volatile`, `wait/notify`.
- `ExecutorService`, пулы, `Future`, `CompletableFuture`.
- `java.util.concurrent` (`ConcurrentHashMap`, `BlockingQueue`).
- Память JVM: heap, stack, GC, метапространство; race condition, deadlock.

**Практика:** параллельная обработка через `ExecutorService` · Producer-Consumer.

---

## Уровень 6. Базы данных и SQL

**Цель:** хранить и читать данные.

**Теория:**
- Реляционные БД (PostgreSQL / MySQL).
- SQL: `SELECT`, `JOIN`, `GROUP BY`, индексы, транзакции.
- JDBC: `PreparedStatement`; ORM, Hibernate / JPA, `EntityManager`; HikariCP.

**Практика:** CRUD на чистом JDBC, затем через JPA · запросы с JOIN.

---

## Уровень 7. Сборка, тесты, Git

**Цель:** работать как в команде.

**Теория:**
- Maven и Gradle: зависимости, фазы сборки.
- Git: ветки, merge, rebase, pull request.
- JUnit 5, Mockito, AAA-паттерн; юнит vs интеграционные тесты.

**Практика:** настроить Maven/Gradle · покрыть логику тестами · замокать через Mockito.

---

## Уровень 8. Spring / Spring Boot

**Цель:** строить реальные веб-приложения.

**Теория:**
- IoC и Dependency Injection, бины, контекст.
- Spring Boot: автоконфигурация, стартеры.
- REST: `@RestController`, `@RequestMapping`, статусы, DTO.
- Spring Data JPA; валидация, `@ControllerAdvice`; `application.yml`, профили; Spring Security + JWT.

**Практика:** REST API To-Do · БД через Spring Data JPA · авторизация по JWT.

---

## Уровень 9. Backend в проде (продвинутый)

**Цель:** выйти на уровень Middle/Senior.

**Теория:**
- Архитектура: слои, чистая архитектура, DDD-основы.
- Микросервисы: REST vs gRPC, API Gateway, service discovery.
- Kafka / RabbitMQ; Redis; Docker, docker-compose, основы Kubernetes.
- CI/CD, мониторинг (Prometheus + Grafana), логирование.
- Паттерны (GoF), SOLID; профилирование, тюнинг JVM/GC.

**Практика:** сервис в Docker + БД через docker-compose · связь двух сервисов через Kafka · кэш Redis.

---

# Часть II. ПРАКТИЧЕСКИЙ КУРС

## 📘 Практический курс по Java

Это — «мясо» роадмапа. Каждый урок построен по одной схеме:

> 🎯 **Цель** → 📖 **Теория** → 💻 **Пример кода** → 🔍 **Разбор** → ⚠️ **Частые ошибки** → 🏋️ **Задание**

Пиши весь код руками. Не копируй — набирай и экспериментируй.

### Содержание курса

| # | Урок | Уровень |
|---|------|---------|
| 1 | Первая программа и как работает Java | 0–1 |
| 2 | Переменные, типы и операторы | 1 |
| 3 | Условия, циклы и методы | 1 |
| 4 | Классы, объекты и инкапсуляция | 2 |
| 5 | Наследование, полиморфизм и интерфейсы | 2 |
| 6 | Коллекции и Generics | 3 |
| 7 | Исключения и работа с файлами | 4 |
| 8 | Лямбды и Stream API | 4 |
| 9 | Мини-проект: консольный менеджер задач | 1–4 |

---

### Урок 1 — Первая программа и как работает Java

🎯 **Цель:** написать, скомпилировать и запустить первую программу; понять, что происходит под капотом.

📖 **Теория.** Java — компилируемый и одновременно платформенно-независимый язык. Исходный файл `.java` компилятор `javac` превращает в байткод `.class`, который выполняет виртуальная машина JVM. Именно поэтому один и тот же байткод работает на Windows, Linux и macOS — принцип *«write once, run anywhere»*.

💻 **Пример кода:**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, Java 2026!");
    }
}
```

Запуск из терминала:

```bash
javac Main.java   # создаёт Main.class (байткод)
java Main         # JVM запускает метод main
```

🔍 **Разбор по строкам:**
- `public class Main` — имя класса должно совпадать с именем файла (`Main.java`).
- `public static void main(String[] args)` — точка входа. JVM ищет именно эту сигнатуру.
- `System.out.println(...)` — вывод в консоль с переводом строки.

⚠️ **Частые ошибки:**
- Имя файла не совпадает с именем public-класса → ошибка компиляции.
- Забытая `;` в конце строки.
- Запуск `java Main.class` вместо `java Main` (надо без расширения).

🏋️ **Задание:** выведи три строки о себе (имя, цель, любимый язык). Запусти двумя способами — из IDE и из терминала.

---

### Урок 2 — Переменные, типы и операторы

🎯 **Цель:** научиться хранить данные и выполнять с ними операции.

📖 **Теория.** В Java есть 8 примитивных типов (`byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`) и ссылочные типы (объекты, массивы, `String`). Примитивы хранят само значение, ссылочные — адрес объекта в памяти.

💻 **Пример кода:**

```java
public class Variables {
    public static void main(String[] args) {
        int age = 25;                 // целое число
        double price = 199.99;        // число с плавающей точкой
        boolean isActive = true;      // логическое
        char grade = 'A';             // символ
        String name = "Anna";         // строка (объект)
        final double PI = 3.14159;    // константа

        int sum = age + 5;
        double total = price * 2;
        boolean adult = age >= 18;

        System.out.println(name + ", " + age + " лет, совершеннолетний: " + adult);
        System.out.println("Сумма: " + sum + ", итого: " + total);
    }
}
```

🔍 **Разбор:** оператор `+` для чисел — сложение, а для строк — конкатенация. `final` делает переменную неизменяемой.

⚠️ **Частые ошибки:**
- `int x = 10 / 3;` даёт `3`, а не `3.33` — целочисленное деление. Для дроби нужен `double`.
- Сравнение строк через `==` вместо `.equals()` — сравнивает ссылки, а не содержимое.
- Переполнение `int` (макс ~2.1 млрд) — для больших чисел бери `long`.

🏋️ **Задание:** напиши программу, которая считает индекс массы тела (BMI) по весу и росту и выводит результат.

---

### Урок 3 — Условия, циклы и методы

🎯 **Цель:** управлять ходом программы и выносить логику в методы.

📖 **Теория.** Условия (`if/else`, `switch`) выбирают ветку выполнения. Циклы (`for`, `while`, `for-each`) повторяют действия. Методы группируют логику и делают код переиспользуемым.

💻 **Пример кода — FizzBuzz + метод:**

```java
public class Logic {
    // метод возвращает строку для одного числа
    static String fizzBuzz(int n) {
        if (n % 15 == 0) return "FizzBuzz";
        if (n % 3 == 0)  return "Fizz";
        if (n % 5 == 0)  return "Buzz";
        return String.valueOf(n);
    }

    public static void main(String[] args) {
        for (int i = 1; i <= 20; i++) {
            System.out.println(fizzBuzz(i));
        }
    }
}
```

🔍 **Разбор:** вынесение логики в метод `fizzBuzz` делает код читаемым и тестируемым. Проверку `% 15` ставим первой — иначе сработает `% 3` и логика сломается.

⚠️ **Частые ошибки:**
- Бесконечный цикл: забыли изменять счётчик в `while`.
- `=` вместо `==` в условии.
- Забытый `break` в `switch` → «fall-through» (провал в следующий case).

🏋️ **Задание:** напиши метод `boolean isPrime(int n)` и выведи все простые числа до 100.

---

### Урок 4 — Классы, объекты и инкапсуляция

🎯 **Цель:** научиться описывать сущности классами и защищать их данные.

📖 **Теория.** Класс — это шаблон, объект — его экземпляр. Инкапсуляция — это скрытие полей (`private`) и доступ к ним только через методы (getter/setter). Это защищает объект от невалидных состояний.

💻 **Пример кода — банковский счёт:**

```java
public class Account {
    private final String owner;
    private double balance;   // поле скрыто

    public Account(String owner, double initial) {
        this.owner = owner;
        if (initial < 0) throw new IllegalArgumentException("Баланс не может быть отрицательным");
        this.balance = initial;
    }

    public void deposit(double amount) {
        if (amount <= 0) throw new IllegalArgumentException("Сумма должна быть > 0");
        balance += amount;
    }

    public void withdraw(double amount) {
        if (amount > balance) throw new IllegalStateException("Недостаточно средств");
        balance -= amount;
    }

    public double getBalance() { return balance; }   // getter

    @Override
    public String toString() {
        return owner + ": " + balance + " ₽";
    }
}
```

🔍 **Разбор:** поле `balance` нельзя изменить напрямую — только через `deposit`/`withdraw`, которые проверяют корректность. `final` у `owner` гарантирует, что владелец не меняется.

⚠️ **Частые ошибки:**
- Публичные поля (`public double balance`) — нарушают инкапсуляцию.
- Отсутствие валидации в конструкторе → объект может родиться в невалидном состоянии.

🏋️ **Задание:** добавь метод `transfer(Account to, double amount)` и проверь перевод между двумя счетами.

---

### Урок 5 — Наследование, полиморфизм и интерфейсы

🎯 **Цель:** переиспользовать код и писать гибкие абстракции.

📖 **Теория.** Наследование (`extends`) позволяет одному классу расширять другой. Полиморфизм — это вызов одного метода у разных объектов с разным поведением. Интерфейс задаёт контракт («что умеет»), не реализацию.

💻 **Пример кода — фигуры:**

```java
interface Shape {
    double area();   // контракт
}

class Circle implements Shape {
    private final double r;
    Circle(double r) { this.r = r; }
    public double area() { return Math.PI * r * r; }
}

class Rectangle implements Shape {
    private final double w, h;
    Rectangle(double w, double h) { this.w = w; this.h = h; }
    public double area() { return w * h; }
}

public class Shapes {
    public static void main(String[] args) {
        Shape[] shapes = { new Circle(2), new Rectangle(3, 4) };
        for (Shape s : shapes) {
            // полиморфизм: вызывается нужная реализация area()
            System.out.printf("Площадь: %.2f%n", s.area());
        }
    }
}
```

🔍 **Разбор:** массив хранит `Shape`, но каждый элемент — свой класс. Вызов `s.area()` выбирает реализацию во время выполнения — это и есть полиморфизм.

⚠️ **Частые ошибки:**
- Глубокая иерархия наследования вместо композиции — хрупкий код.
- Забытый `@Override` — можно случайно создать новый метод вместо переопределения.

> 💡 **Правило:** *«Композиция лучше наследования»* — влагай объекты как поля, а не строй длинные цепочки `extends`.

🏋️ **Задание:** добавь класс `Triangle` и посчитай суммарную площадь всех фигур в массиве.

---

### Урок 6 — Коллекции и Generics

🎯 **Цель:** выбирать правильную структуру данных и писать типобезопасный код.

📖 **Теория.** `List` — упорядоченный список с дублями. `Set` — без дублей. `Map` — пары ключ-значение. Generics (`<T>`) дают проверку типов на этапе компиляции.

Сложность операций (Big-O):

| Структура | Доступ | Вставка | Поиск |
|----------|--------|---------|-------|
| `ArrayList` | O(1) | O(1)* | O(n) |
| `LinkedList` | O(n) | O(1) | O(n) |
| `HashMap` | — | O(1) | O(1) |
| `TreeMap` | — | O(log n) | O(log n) |

💻 **Пример кода — частотный словарь:**

```java
import java.util.*;

public class WordCount {
    public static void main(String[] args) {
        String text = "java is great and java is fast";
        Map<String, Integer> freq = new HashMap<>();

        for (String word : text.split(" ")) {
            freq.merge(word, 1, Integer::sum);  // увеличиваем счётчик
        }

        freq.forEach((word, count) ->
            System.out.println(word + " = " + count));
    }
}
```

🔍 **Разбор:** `merge(key, 1, Integer::sum)` — если ключа нет, кладёт 1; если есть — прибавляет. Это короче, чем ручная проверка `containsKey`.

⚠️ **Частые ошибки:**
- Изменение коллекции во время итерации → `ConcurrentModificationException`.
- Использование объекта без `equals/hashCode` как ключа `HashMap`.
- Выбор `LinkedList` «потому что быстрее» — на деле `ArrayList` быстрее почти всегда.

🏋️ **Задание:** реализуй свой класс `Stack<T>` на базе `ArrayList` с методами `push`, `pop`, `peek`, `isEmpty`.

---

### Урок 7 — Исключения и работа с файлами

🎯 **Цель:** писать код, который не падает от ошибок.

📖 **Теория.** Checked-исключения проверяются компилятором (`IOException`), unchecked — нет (`NullPointerException`). `try-with-resources` автоматически закрывает ресурсы.

💻 **Пример кода — чтение файла:**

```java
import java.io.IOException;
import java.nio.file.*;
import java.util.List;

public class FileReader {
    public static void main(String[] args) {
        Path path = Path.of("data.txt");
        try {
            List<String> lines = Files.readAllLines(path);
            System.out.println("Строк: " + lines.size());
            lines.forEach(System.out::println);
        } catch (IOException e) {
            System.err.println("Не удалось прочитать файл: " + e.getMessage());
        }
    }
}
```

🔍 **Разбор:** `Files.readAllLines` бросает checked `IOException` — его обязательно обработать. Мы ловим его и выводим понятное сообщение вместо падения.

⚠️ **Частые ошибки:**
- Пустой `catch {}` — проглатывает ошибку и скрывает проблему.
- Ловля `Exception` вместо конкретного типа.
- Ручное закрытие файлов вместо `try-with-resources` → утечки ресурсов.

🏋️ **Задание:** напиши своё исключение `InvalidAgeException` и бросай его, если возраст < 0.

---

### Урок 8 — Лямбды и Stream API

🎯 **Цель:** писать краткий декларативный код для обработки коллекций.

📖 **Теория.** Лямбда — короткая функция без имени: `x -> x * 2`. Stream API позволяет обрабатывать данные цепочкой операций (`filter`, `map`, `collect`) вместо ручных циклов.

💻 **Пример кода — фильтр и преобразование:**

```java
import java.util.*;
import java.util.stream.*;

public class Streams {
    record User(String name, int age) {}

    public static void main(String[] args) {
        List<User> users = List.of(
            new User("Anna", 25),
            new User("Boris", 17),
            new User("Clara", 30),
            new User("Dmitry", 16)
        );

        // взрослые, отсортированные по имени
        List<String> adults = users.stream()
            .filter(u -> u.age() >= 18)
            .sorted(Comparator.comparing(User::name))
            .map(User::name)
            .collect(Collectors.toList());

        System.out.println(adults);   // [Anna, Clara]

        double avgAge = users.stream()
            .mapToInt(User::age)
            .average()
            .orElse(0);
        System.out.printf("Средний возраст: %.1f%n", avgAge);
    }
}
```

🔍 **Разбор:** поток ленивый — промежуточные операции (`filter`, `map`) выполняются только при терминальной (`collect`). `Optional` от `average()` защищает от пустого результата.

⚠️ **Частые ошибки:**
- Изменение внешних переменных внутри лямбды (нужны effectively final).
- Злоупотребление `Stream` там, где обычный цикл проще и читаемее.
- `.get()` у `Optional` без проверки → исключение.

🏋️ **Задание:** сгруппируй пользователей по возрастным группам (несовершеннолетние/взрослые) через `Collectors.groupingBy`.

---

### Урок 9 — Мини-проект: консольный менеджер задач (To-Do)

🎯 **Цель:** собрать всё изученное в одном небольшом приложении: классы, коллекции, стримы и обработка ввода.

💻 **Код:**

```java
import java.util.*;
import java.util.stream.*;

public class TodoApp {
    record Task(int id, String title, boolean done) {
        Task complete() { return new Task(id, title, true); }
    }

    private final List<Task> tasks = new ArrayList<>();
    private int nextId = 1;

    void add(String title) {
        tasks.add(new Task(nextId++, title, false));
    }

    void complete(int id) {
        for (int i = 0; i < tasks.size(); i++) {
            if (tasks.get(i).id() == id) {
                tasks.set(i, tasks.get(i).complete());
                return;
            }
        }
        System.out.println("Задача #" + id + " не найдена");
    }

    void print() {
        if (tasks.isEmpty()) { System.out.println("Список пуст"); return; }
        tasks.forEach(t ->
            System.out.printf("[%s] #%d %s%n", t.done() ? "x" : " ", t.id(), t.title()));
        long left = tasks.stream().filter(t -> !t.done()).count();
        System.out.println("Осталось: " + left);
    }

    public static void main(String[] args) {
        TodoApp app = new TodoApp();
        app.add("Изучить коллекции");
        app.add("Написать To-Do");
        app.add("Сделать пет-проект");
        app.complete(2);
        app.print();
    }
}
```

🔍 **Разбор:** `Task` — неизменяемый `record`; при выполнении создаётся новый объект вместо мутации. Подсчёт оставшихся задач — через Stream API.

🏋️ **Задания по расширению:**
1. Добавь чтение команд с клавиатуры через `Scanner`.
2. Сохраняй задачи в файл и загружай при старте (Урок 7).
3. Добавь фильтр «показать только невыполненные».
4. Покрой логику юнит-тестами (Уровень 7 роадмапа).

> 🏆 Готово! Если ты сделал этот проект сам — ты уже владеешь основами Core Java. Следующий шаг — Уровень 5–6 роадмапа.

---

# Часть III. ДОПОЛНИТЕЛЬНО

## 🚀 Pet-проекты по уровням

| Уровень | Проект |
|---------|--------|
| 1–2 | Консольный менеджер задач (To-Do) |
| 3–4 | Анализатор логов / CSV со Stream API |
| 5 | Многопоточный загрузчик файлов |
| 6–7 | Библиотека книг с БД и тестами |
| 8 | REST API интернет-магазина (Spring Boot + JPA) |
| 9 | Микросервисное приложение (Docker + Kafka + Redis) |

---

## 📚 Полезные ресурсы

- **Документация:** официальные Oracle Java Tutorials, Spring Docs.
- **Книги:** «Head First Java», «Effective Java» (Bloch), «Java Concurrency in Practice».
- **Практика:** LeetCode, Codewars, Exercism (трек Java).
- **Курсы:** современные курсы по Java 21 и Spring Boot 3.

---

## ✅ Чек-лист готовности к Junior-собеседованию

- [ ] Уверенно знаю ООП и могу привести примеры
- [ ] Знаю коллекции и их сложность (Big-O)
- [ ] Умею писать Stream API и лямбды
- [ ] Понимаю основы многопоточности
- [ ] Пишу SQL и работаю с JPA
- [ ] Сделал хотя бы 1 проект на Spring Boot
- [ ] Покрываю код тестами и работаю с Git

---

> 💡 **Главный принцип:** учить → сразу применять → строить проект. Удачи в прокачке! ☕

