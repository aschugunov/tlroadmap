# Выбор и контроль технологий
## Описание
Периодически команда разработки начинает использовать новые технологии. Это может происходить как по рациональным причинам – начинаете решать новый тип задач, модернизируете архитектуру, так и не очень – разработчикам хочется попробовать на практике то, о чем они услышали на конференции. Роль тимлида заключается в том, чтобы отвечать за рациональность используемого стека технологий и построить процесс их ввода и вывода из использования. 

Под технологиями здесь понимается всё – языки, фреймворки, библиотеки, инструменты.

## Почему ветка важна?
Для тимлида:
- Без контроля за тем, какие технологии используются, область ответственности может быстро выйти из под контроля
Тимлид обладает более широким контекстом, чем разработчики, чтобы оценить риски от внедрения новых технологий

Для команды:
- Если есть понятный процесс тестирования и внедрения новых технологий, это может быть хорошим кандидатом в качестве личных целей

Для компании:
- Упрощается унификация знаний между разными командами разработки и появляется возможность перебрасывать людей между командами
- Понижается риск того, что важный компонент системы будет написан с использованием чего-то экзотичного

## Что будет, если её не делать?
- Команда разработки будет внедрять новые технологии исходя только из своей заинтересованности
  - Усложняется найм людей, так как на входе требуется больше знаний
  - Повышаются риски безопасности, так как больше мест для нахождения уязвимостей
  - Сложнее перекидывать людей между проектами и компаниями, так как навыки не будут универсальными
  - Система в целом становится менее поддерживаемой
- Внедрение любых новых технологий может быть под запретом
  - Усложняется найм людей, так как им не будет интересно копаться в старых технологиях
  - Понижается мотивация существующей команды
  - Не используются более эффективные способы решения старых задач

## На кого может быть делегирована?
На самых опытных разработчиков отдельных платформ или направлений.

## Примеры поведения
### Примеры плохого поведения
- Разработчики с порога могут втаскивать в production любую технологию
- Процесс принятия решения о внедрении новых технологий слишком бюрократизирован
- Когда принимается решение об отказе от использования какой-то технологии, нет плана по полному избавлению от неё
- При принятии решения о внедрении технологии учитывается мнение только одной группы – разработчиков, архитекторов, менеджеров или кого-то ещё

### Примеры хорошего поведения
- Есть чек-лист вопросов, на которые надо ответить при вводе или выводе технологии из стека
- Есть готовые подходы по тому, как можно аккуратно попробовать новую технологию и дёшево от неё отказаться
- Технический стек компании актуален на рынке
- Если появляется новая технология, которая может принести проекту пользу, её внедрение не является сложной проблемой
- Вся команда знает, как в проект можно внедрить новую технологию

## Способы прокачки
### Практика
[Технологический радар](https://www.thoughtworks.com/radar) — это набор практик, описывающих жизненный цикл технологии, и инструмент визуализации текущего состояния технологического стека. Радар помогает ответить на ряд вопросов. Вот примеры:
- Почему мы не используем технологию X?
- Как мы относимся к модной технологии Y?
- Что стоит использовать в разработке нового сервиса?
- На какие технологии мне стоит сделать упор в саморазвитии?
- Какие технологии и почему не востребованы в моей компании?

По сути, это диаграмма состояний технологий. которая отображает:
- Текущий статус использования технологии в компании
  - ASSESS – присматриваемся, но пока не используем в production, аккуратно тестируем на маленьких проектах
  - TRIAL – тестируем, но не на критичном компоненте
  - ADOPT – смело используем в production
  - HOLD – по какой-то причине перестали использовать
- Принадлежность к категории
  - Языки
  - Фреймворки
  - Инструменты для работы с данными
  - Процессы

#### Создание радара
1. Соберите группу экспертов в определённой платформе или направлении (iOS, Android, backend, frontend)
2. Попросите каждого на стикерах перечислить все технологии, которые сейчас используются в вашем продукте, от которых когда-то отказались, или к которым хочется присмотреться
3. Объедините получившиеся стикеры по категориям. Это могут быть языки, фреймворки, библиотеки – что угодно, что имеет для вас смысл.
4. Внутри категории разбейте все стикеры по статусам – Assess, Trial, Hold, Adopt.
5. Для каждой из технологий постарайтесь собрать краткую историю того, как она оказалась в этом статусе.
6. Соберите с помощью [конструктора](https://www.thoughtworks.com/radar/byor) свой собственный радар и внесите туда всю информацию.
7. Повторите этот процесс для других платформ.

#### Использование радара
1. Кратко опишите процессы перехода технологии между статусами. Это удобно делать с помощью чек-листов.
2. Договоритесь о том, какие люди в компании принимают решение о переходе технологии между статусами. Это может быть CTO или комитет из экспертов.
3. Периодически пересматривайте текущее состояние радара и проверяйте, что он соответствует действительности.

#### Пример требований для перехода между статусами
##### Из состояния неопределённости в ASSESS
Тот, кто хочет внедрить новую технологию, отвечает на вопросы:
- Задачи, которая должна решать указанная технология в компании
- Action Plan внедрения технологии: шаги, сроки, критерии готовности
- Конкуренты технологии внутри компании и снаружи, преимущества и недостатки по сравнению с конкурентами
- Оценочный уровень зрелости технологии
- Оценочное количество людей, знакомых с технологией внутри компании
- Оценочное количество людей, знакомых с технологией на рынке труда в России

Решение принимает тимлид команды, в которой планируется внедрение.

##### Из ASSESS в TRIAL
Технология должна быть опробована на каком-то тестовом проекте, который позволит понять её плюсы и минусы. За ревью результатов тестирования отвечает тимлид команды, в которой проводилось внедрение, плюс один или два эксперта из соседних команд.

##### Из TRIAL в ADOPT
Технология должна быть опробована в production той командой, которая начала её внедрение. За ревью результатов этого этапа отвечают руководители направлений и CTO.

##### Из любого статуса в HOLD
Тот, кто хочет избавиться от технологии, должен ответить на вопросы:
- Почему надо прекратить использовать технологию
- Кого в компании касается это решение
- На что технология будет заменена

## Консультации
- [Telegram-чат TL Bootcamp](https://tlinks.run/tlbootcamp)

## Теория
### Статьи
**Раскрывают тему:**
- [Build Your Own Technology Radar](https://www.thoughtworks.com/radar/byor)

**Дополнительные материалы:**
- [Радар технологий: перечень языков, инструментов и платформ, которые прошли через руки Lamoda](https://habr.com/ru/company/lamoda/blog/428411/)
- [Avito Tech Radar](https://techradar.avito.ru/)

### Прочие материалы
- [StackShare – база данных технологических стеков разных компаний](https://stackshare.io/)