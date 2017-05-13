Вопросы на собеседование iOS-разработчика
==
Тем: 20 | Вопросов: свыше 150 

<span style="font-family: 'Raleway';">

</span>

Objective-C, Foundation:
------------------------
- Что такое `свойство`?
- Как правильно реализовать сеттер для свойства с параметром retain?
- Директива `@synthesize`, `@dynamic`, чем отличаются друг от друга?
- В чем разница между `точечной нотацией` и использованием квадратных скобок?
- Есть ли `приватные и защищенные` методы в Objective-C? 
- Чем `категория` отличается от `категории продолжения класса` (extension, наименованная категория)?
- Можно ли добавить `ivar` в категорию?
- Когда лучше использовать `категорию`, а когда `наследование`?
- Как имитировать `множественное наследование`?
- Можно ли чтобы разные классы реализовывали один протокол. (ClassA, ClassB и ClassC - реализуют ClassCProtocol)?
- `Формальный и неформальный (informal)` протокол? `Протоколы (protocols)`: основные отличия между c#/java интерфейсами и Objective-C протоколами? Что делать в случае если класс не реализует какой-то метод из протокола?
- Почему нам не следует вызывать `instance методы в методе -init (initialize)`?
- Что такое `назначенный инициализатор (designated initializer)`? Приведите пример назначенного инициализатора (имеется ввиду `if (self  = [super ...])`)?
- Что происходит когода мы пытаемся вызвать метод у nil указателя? Разница между nil и Nil и [NSNull null]?
- Что такое `селектор (selector)`? Как его вызвать? как отложить вызов селектора? Что делать если селектор имеет много параметров? `(NSInvocation)`
- Что такое `быстрое перечисление (fast enumeration)`? 
- Что такое `делегат (delegate)`? 
- Что такое `notifications (уведомления)`?
- Какая разница между использованием `делегатов (delegation)` и `нотификейшенов (notification)`?
- Какая разница между использованием селекторов, делегатов и блоков?
- В чем отличия KVC-KVO?
- Что такое `KVO`? Когда его нужно использовать? Методы для обозревания объектов? Работает ли `KVO с instance переменными (полями)` объекта?
- Что такое `KVC`? Когда его нужно использовать?
- Какие существуют `root классы` в iOS? Для чего нужны `root классы`? 
- Как работает `proxy`?
- Что такое `тип id`. Что случится во время компиляции если мы посылаем сообщение объекту `типа id`? Что случится во время выполнения если этот метод существует?
- Цепочка ответсвенности, что происходит с методом после того как он не нашелся в объекте класса, которому его вызвали (в сторону forwardInvocation:)?
- Что такое `указатель isa`? Для чего он нужен?
- В чем разница между `NSArray и NSMutableArray`? непотоко-безопасный NSMutableArray?
- Чем отличается `NSSet от NSArray`? Какие `операции` происходят быстро в `NSSet` и какие в `NSArray`?
- Как удалить объект в ходе итерации по циклу?
- Как лучше всего загрузить `UIImage c диска(с кеша)`?
- Какой контент лучше хранить в `Documents`, а какой в `Cache`?
- `NSCoding, archiving`?
- Протокол `NSCopying`, почему мы не можем просто использовать любой собственный объект в качестве ключа в словарях (NSDictionary) , что нужно сделать чтобы решить эту проблему? (разница между глубоким и поверхностным копированием)?
- Суть `рантайма (Runtime), отправление сообщения`? Как работает Runtime?
- Как добавить свойство в существующий объект с закрытой реализацией? Можно ли это сделать через runtime?
- Что представляет собой объект NSError?
- Что такое динамическая диспетчеризация (Dynamic Dispatch)?
- Сколько различных аннотаций (annotations) доступно в Objective-C?
- Пожалуйста, объясните ключевое слово (keyword) final в классе?
- Какую проблему решает делегирование?
- Почему мы используем шаблон делегата для уведомления о событиях текстового поля?
- What is the difference Delegates and Callbacks ?


Memory Management:
------------------
- Объявление свойств c атрибутами: `retain`, `assign`, `nonatomic`, `readonly`, `copy`, `weak`, `strong`, `unsafe_unretained`?
- Реализуйте следующие методы: `retain/release/autorelease`?
- Почему мы не используем strong для enum свойств?
- Как происходит `ручное управление памятью - MRC` в iOS?
- `autorelease vs release`?
- Что означает `ARC`?
- Что делать, если проект написан с использованием ARC, а нужно использовать классы сторонней библиотеки написанной без ARC?
- `Atomic vs nonatomic`. Чем отличаются? Как вручную переопределить atomic/nonatomic сеттер в не ARC коде?
- Вопрос о `циклах в графах владения` (retain cycle)? 
- Как `использовать` self внутри блоков? Приведите пример `retain cycle` в блоке?
- Зачем все свойства ссылающиеся на делегаты `strong для ARC и retain для MRC`? :))) 
- Что такое `autorelease pool`?
- Что такое `runLoop` `(NSAutoreleasePool)`, когда он используется? `(timers, nsurlconnection ...)`?
- Как связаны `NSRunLoop и NSAutoreleasePool` на пальцах?
- Как можно заимплементировать `autorelease pool на с++`?
- Если я вызову `performSelector:withObject:afterDelay:` - объекту пошлется сообщение retain?
- Как происходит обработка `memory warning`(предупреждение о малом  количестве памяти)? Зависит ли обработка от версии iOS, как мы должны их обрабатывать?
- Напишите простую реализацию `NSAutoreleasePool` на Objective-C?
- Когда нужно использовать метод `retainCount` (никогда, почему?) :)))
- Что случится если вы добавите только что созданный объект в `Mutable Array`, и пошлете ему сообщение `release`? Что случится если послать сообщение `release` массиву? Что случится если вы удалите объект из массива и попытаетесь его использовать?
- С подвохом: как работает `сборщик мусора` в iOS? :)))
- Нужно ли `ретейнить` (посылать сообщение retain) `делегаты`?
- Для чего используется класс `NSCoder`?
- Опишите правильный способ управления памятью выделяемой под `Outlet'ы`?

Networking:
----------
- Преимущества и недостатки `синхронного и асинхронного` соединения?
- Что означает `http, tcp`?
- REST, HTTP, JSON. Что это?
- Какие различия между `HEAD, GET, POST, PUT`? 
- Как загрузить что-то из интернета? В чем разница между `синхронными и асинхронными запросами`? Небольшое задание. Опишите как загрузить изображение из интернета и отобразить его в ImageView — все это должно происходить после нажатия кнопки.
- Что такое REST (Restful)?
- Какую JSONSerialization имеет ReadingOptions?
- Объясните различия в SOAP и REST?

Multithreading:
---------------
- Зачем мы используем synchronized?
- В чем разница между синхронным и асинхронным таском (задачей)?
- Что такое блоки (blocks)?
- Какие типы блоков вы знаете (глобальные/локальные, heap/stack)?
- Что такое обработчик завершения (completion handler)?
- Что такое параллелизм (concurrency)?
- Блокировки читателей-писателей (readers-writers lock)?
- С подвохом: вопрос о несуществующем параметре `atomic`, что он означает? Приведите пример кейса с использованием `atomic`?
- Как многопоточность работает с `UIKit`?
- Как запустить селектор в `(фоновом) потоке`?
- Как запустить `поток (thread)`? Что первым нужно сделать при запуске `потока`?
- Что такое `GCD`? Как `GCD` связан с многопоточностью? Типы queue и queue == thread?
- `NSOperation` vs `GCD`?
- Что такое Dispatch Group?
- NSOperation — NSOperationQueue — NSBlockOperation?
- Что такое `deadlock`?
- Что такое `livelock`?
- Что такое `семафор (semafor)`?
- Что такое `мьютекс (mutex)`?
- `Асинхронность` vs `многопоточность`. Чем отличаются?
- Какие технологии в iOS возможно использовать для работы с потоками. Преимущества и недостатки.
- Как запустить поток? Что первым нужно сделать при запуске потока? (NSAutoreleasePool - пул автоосвобождения) Что такое runLoop, кодга он используется? (timers, nsurlconnection …)
- Чем отличается `dispatch_async от dispatch_sync`?
- Для чего при разработке под iOS использовать `POSIX-потоки`? `pthread_create(&thread, NULL, startTimer, (void *)t);`
- А чем реально `POSIX-потоки` лучше чем `GCD или NSOperationQueue вместе с NSOperation`? Приходилось ри реально использовать POSIX и как в этом были прюсы? Реально, просто интересно…
 `Use POSIX calls if cross-platform portability is required. If you are writing networking code that runs exclusively in OS X and iOS, you should generally avoid POSIX networking calls, because they are harder to work with than higher-level APIs. However, if you are writing networking code that must be shared with other platforms, you can use the POSIX networking APIs so that you can use the same code everywhere. `

UIKit:
------
- Разница между свойствами `bounds и frame` объекта UIView? Понимание системы координат?
- Цикл жизни `View Controller`?
- Что такое `View` (представление) и что такое `window` и цикл жизни `UIView`?
- Что такое `Responder Chain` (цепочка обязанностей, `паттерн chain of responsibility`, на примере UI компонентов iOS ), `becomeFirstResponder`.
- Что означают `IBOutlet` и `IBAction`, для чего они нужны, и что значат для препроцессора?
- Как работает `UITableView`? Жизненный цикл UITableView?
- Что можно сделать если клавиатура при появлении скрывает важную часть интерфейса?
- Почему мы должны `релизить IBOutlet'ты` во viewDidUnload?
- Что такое `awakeFromNib`, в чем разница между `xib и nib` файлами?
- Иерархия наследования UIButton.
- В чем разница CollectionViews & TableViews?
- Что такое UIStackView?
- Какая ваша любимая библиотека визуализации диаграмм (visualize chart library)?
- Что такое Autolayout?

CoreData, Persistency:
----------------------
- Какие есть типы хранилищ (data percistency) и какую стратегию хранения использовать в том или ином случае?
- Какие есть лимиты у JSON/PLIST?
- Что такое Keychain?
- Какие есть лимиты у SQLite?
- Какие есть преимущества у Realm?
- Что такое `нормализация` данных?
- Что такое `Core Data`?
- Что такое NSFetchRequest?
- Что такое NSPersistentContainer?
- Использовали ли `NSFetchedResultsController`? Почему? 
- Что такое `контекст (Managed object context)`? Как происходят `изменения в NSManagedObjectContext`?
- Что такое `Persistent store coordinator`? Зачем нужен `NSPersistentStoreCoordinator`?
- Зачем нужно делать `двустороннии связи` в таблицах?
- Что таке `Fetched Property` и особенности работы с ним по сравнению с обычной связью?
- Что такое `Fault` и зачем он нужен?
- В каких случаях лучше использовать `SQLite`, а в каких `Core Data`?
- Какие есть нюансы при использовании `Core Data в разных потоках`? Как `синхронизировать данные между потоками`(Как синхронизировать контекст)? Синхронизация разных типов NSManagedObjectContext (получение и изменение данных в child контекстах)? 
- Как использовать `СoreData` совместно с `многопоточностью`?
- Что такое `NSManagedObjectId`? Можем ли мы сохранить его на потом если приложение закроется?
- Какие `типы хранилищ` поддерживает CoreData?
- Что такое `ленивая загрузка (lazy loading)`? Что ее связывает с CoreData? Опишите ситуация когда она может быть полезной?
- Составить SQL запрос на выборку всех проектов  на которых сидит девелопер с id ==3. (Developers:id,name; Projects:id,name; Developers&Projects:project_id,developer_id)?

CoreAnimation, CoreGraphics:
----------------------------
- Что такое `CALayer`? 
- Чем отличается `UIView от CALayer`?
- Какие типы `CALayer` есть?
- Чем отличается `UIView based Animation от Core Animation`?
- Можно ли `отследить изменение alpha`, через KVO в CALayer?
- Тайминги в `CoreAnimation`?
- Что такое `backing store`?
- Чем отличаются `аффинные преобразования от трехмерных`?
- Нужно ли `ретейнить (посылать сообщение retain)` делегат для `CAAnimation`?

iOS Platform:
------------
- Какие бывают `состояния` (states) у приложения?
- Жизненный цикл приложения?
- Каковы самые важные методы делегирования в приложении, с которыми будет сталкиваться разработчик?
- Какого разрешение экранов iphon'ов, и в чем разница между `points (точками)` и `пикселями (pixels)`?
- Что такое `responder chain`?
- Какие типы нотификаций есть в iOS?
- Как работают `push нотификации`?
- Какие ограничение есть у платформы iOS?
- Какие ограничение есть у платформы tvOS?
- Что такое Code Coverage (покрытие кода)?
- Что делает подписание кода (code signing)?
- Что такое TVMLKit?
- Что такое ABI?
- Что такое #keyPath()?
- Что IGListKit дает разработчикам?
- Каковы три основных улучшения отладки в Xcode 8?
- Что такое биткод (bitcode)?
- Какие есть ограничения (limits) у SiriKit?
- Что нового в iOS 10?
- Что такое GraphQL?
- What is the biggest changes in UserNotifications?
- Как получить токен устройства (device token)?
- Какие ограничения (limits) у Remote Notifications?

Architecture
------------
- Если вам нужно сделать рефакторинг, с чего бы вы начали?
- SOLID?
- Что такое protocol oriented programming?
- Алгоритмическая сложность (big-o notation)?
- Что такое `VIPER` архитектура?
- What is the difference open & public access level?
- What is the difference fileprivate & private access level?
- Что такое внутренний доступ (internal access)?
- Что такое `TDD` vs.`BDD`?
- Что такое `DDD`?
- Расскажите о `паттерне MVC`. Чем отличается `пассивная` модель от `активной`?
- Паттерн `MVC vs MVP vs MVVM`? https://habrahabr.ru/post/215605/
- Принципы `DRY`?
- Принципы `KISS`? 
- Что такое `IoC`? 
- Где мы используем Dependency Injection?
- Когда подходящее время для внедрения зависимостей (dependency injection) в наши проекты?
- Explain Priority Inversion and Priority Inheritance?
- Clean Architecture?
- Каковы главные цели фреймворков (framework)?
- Which of the communication methods allows for a loosely coupled, one-to-many pattern and one-to-one pattern?
- Игра в `разбитые окна`?
- Объясните разницу между SDK и Framework?
- В чем недостаток жесткого кодирования? (What is the disadvantage to hard-coding log statements?)

Unit Testing
-----------
- Что такое RGR ( Red — Green — Refactor )?
- Объясните “Arrange-Act-Assert”?
- Какие преимущества в написании тестов в приложениях?
- Опишите Test Driven Development в трех простых правилах?
- Что такое TDD?
- Что такое Continuous Integration?
- Чем отличается Mock от Stub. (mock - имитация поведения, stub - вводные данные)

Programming:
--------
- Что такое `куча (heap)` и `стэк (stack)`? В какой памяти создаются объекты, примитивные типы и блоки?
- Что такое `полиморфизм`?
- Что такое `инкапсуляция`? Что такое `нарушение инкапсуляции`?
- Чем `абстрактный класс` отличается от `интерфейса`?
- Что такое сериализация объекта?
- Что такое `регулярные выражения` (regular expression)?
- Что такое `перегрузка операторов (operator overloading)`?
- Что такое `указатель` (pointer)?
- Что такое `функция` (function)?
- Как передавать переменную как ссылку?
- Что такое `класс`?
- Что такое `объект`?
- Что такое `интерфейс`?
- Когда и почему мы используем объект вместо структур?

General:
--------
- Ваше любимое видео с WWDC?
- Какое ваше любимое приложение и почему?
- Что нового появилось в iOS 10/iOS 9?
- Что такое парное программирование?
- Что такое ограничивающая рамка (bounding box)?
- Сколько есть API'шек для эффективного отслеживания местоположения?
- Какое самое главное преимущество у Swift?
- Что делает React Native специальным для iOS?
- Что означает бритье Яка (Yak Shaving)?
- Каковы пять основных практических рекомендаций для улучшения типографического качества (typographic quality) мобильных проектов?
- Что такое Alamofire?
- Вы раньше работали в качестве подрядчика?Have you worked as a contractor before?
- Что такое управление зависимостями (Dependency Management)?
- Что такое диаграммы классов UML?

Паттерны:
--------
- Что такое паттерн `Фабрика` (Factory)?
- Что такое паттерн `Фасад` (Facade)?
- Что такое паттерн `Декоратор` (Decorator)?
- Что такое паттерн `Адаптер` (Adapter)?
- Что такое паттерн `Наблюдатель` (Observer)?
- Что такое паттерн `Мементо` (Memento)?
- Реализация `Cинглтона` (Singleton) в `ARC` и в `non-ARC`?
- Назовите основные отличия `синглтона` от `статического класса`, и когда следует использовать один, а когда другой? 
- Как пересоздать синглтон? Можно ли `обнулить объект синглтона`?

Git:
----
- В чем разница между SVN и Git?
- Какая команда Git позволяет объединить коммиты?
- Какая команда Git позволяет нам найти плохие коммиты?
- Какая команда Git сохраняет ваш код без коммита?

Структуры данных:
----------------
- Что такое Б-деревья (B-Trees)?

С:
---
- Как представлены `Си-структуры` (CGRect, CGSize, CGPoint) в Objective-C?

Algorithms:
----------
- Напишите код, который `разворачивает строку на С++`. (переставить символы в строке в обратном порядке)?
- Поменять местами a и b не используя промежуточную переменную?
- Написать функцию вычисления n-го числа последовательности фебоначи. (если решить через рекурсию, спросят чем опасно такое решение)?
- Решить задачку о массиве: дан массив из 1001 элемента в котором присутсвуют все числа от 1 до 1000 и одно повторяется дважды, узнать какое, если к каждому элементу можно обратиться только 1 раз?
- Как из строки вытащить подстроку?
- В массиве 1001 число в диапазоне от 1 до 1000 включительно. Лишь одно число в массиве повторяется дважды. Надо за линейное время (и обратившись к каждому числу максимум один раз) найти продублированное число.

Logical:
--------
- Есть 4 человека, каждый проходит мост за 1, 2, 5, и 10 минут соответственно. Через мост они могут переходить только парами, держась за руку и только с фонариком. Притом один должен вернуться обратно и передать фонарик. Необходимо переправить всех за 17 мин на другую сторону. Задача решаема.

Code Puzzels:
-------------

- Что произойдет здесь (компиляция  + время выполнения): 

```objc
NSString *s = [NSNumber numberWithInt:3]; 
int i = [s intValue];
```

- Что не так с этим кодом? Зачем нужны `инициализаторы`?

```objc
[[[SomeClass alloc] init] init];
```

- Сработает ли `таймер`? Почему? 

```objc
void startTimer(void *threadId) {
   [NSTimer  scheduleTimerWithTimeInterval:10.0f 
      target:aTarget 
          selector:@selector(tick: ) 
          userInfo:nil
           repeats:NO];
}

pthread_create(&thread, NULL, startTimer, (void *)t);
```

- Какой метод вызовется: класса A или класса B? Как надо изменить код, чтобы вызвался метод класса A?

```objc
@interface A : NSObject
- (void)someMethod;
@end

@implementation A
- (void)someMethod {
    NSLog(@"This is class A");
}
@end

@interface B : A
@end

@implementation B
- (void)someMethod  {
    NSLog(@"This is class B");
}
@end

@interface C : NSObject
@end

@implementation C
- (void)method  {
    A *a = [B new];
    [a someMethod];
}
```

- В каких случаях лучше использовать `strong`, а в каких `copy` для NSString? Почему?

```objc
@property (nonatomic, strong) NSString *someString;
@property (nonatomic, copy) NSString *anotherString;
```

- Что выведется в консоль? Почему?

```objc
- (BOOL)objectsCount {
    NSMutableArray *array = [NSMutableArray new];
    for (NSInteger i = 0; i < 1024; i++) {
        [array addObject:[NSNumber numberWithInt:i]];
    }
    return array.count;
}

- (void)someMethod {
    if ([self objectsCount]) {
        NSLog(@"has objects");
    }
    else {
        NSLog(@"no objects");
    }
}
```

- Выведется ли в дебагер «Hello world»? Почему?

```objc
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    dispatch_sync(dispatch_get_main_queue(), ^{
        NSLog(@"Hello world");
    });

   /* Another implementation */
   return YES;
}
```

- Что выведется в консоль?

```objc
 dispatch_async(dispatch_get_main_queue(), ^
    {
        NSLog(@"A %d", [object retainCount]);
        dispatch_async(dispatch_get_main_queue(), ^{
            NSLog(@"B %d", [object retainCount]);
        });
        NSLog(@"C %d", [object retainCount]);
    });
    NSLog(@"D %d", [object retainCount]);
```

- Что произойдет при исполнении следующего кода? 

```objc
Ball *ball = [[[[Ball alloc] init] autorelease] autorelease];
```
Additional:
-----------------------------
- Анкета в которой просят оценить свои знания по технологиям по 10 бальной шкале.
 1. Objective-C
 2. C
 3. Swift
 4. iOS Platform
 5. Architecture
 6. Memory Management
 7. Multithreading
 8. UIKit
 9. CoreData, Persistency
 10. Design Patterns
 11. Unit Testing
 12. Git
 13. Core Animation
 14. Algorithms and Data Structure
 15. Networking



Swift
----------
- `Фундаментальные` типы и `коллекции`? 
- Aттрибут `@UIApplicationMain` ?
- Что такое `Bridge Header`? Как использовать Objective-C код в Swift проекте?
- Оператор `guard`?
- `Интерполяция` vs `конкатенация` строк?
- `let` vs `var`?
- `typealias`? Создание своего собственного типа?
- nil в Swift vs nil в Objective-C? Различия?
- Оператор `??`?

