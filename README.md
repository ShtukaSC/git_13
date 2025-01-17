# git_13
Задание 1

Активный master-сервер и пассивный репликационный slave-сервер:
- Обеспечение отказоустойчивости: при отказе master-сервера, slave-сервер может продолжать обслуживание запросов, что повышает надежность системы.
- Увеличение производительности: возможность распределения нагрузки между master- и slave-серверами, что позволяет обрабатывать большее количество запросов.
- Легкость масштабирования: добавление дополнительных slave-серверов для увеличения пропускной способности и резервирования данных.
 
Master-сервер и несколько slave-серверов:
- Распределение нагрузки: возможность равномерного распределения запросов между master- и slave-серверами для увеличения производительности.
- Повышение отказоустойчивости: наличие нескольких slave-серверов позволяет обеспечить резервирование данных и продолжение работы при отказе одного из серверов.
- Гибкость конфигурации: возможность настройки различных параметров для каждого slave-сервера в зависимости от требований системы.
  
Активный сервер со специальным механизмом репликации — distributed replicated block device (DRBD):
- Высокая надежность данных: DRBD обеспечивает синхронизацию данных между активным сервером и его репликой, что гарантирует целостность информации.
- Быстрое восстановление после сбоев: возможность быстрого восстановления работы системы благодаря наличию активного сервера и готовой к работе реплики.
- Эффективное использование ресурсов: DRBD позволяет использовать ресурсы серверов более эффективно за счет репликации данных и распределения нагрузки.
 
SAN-кластер:
- Высокая отказоустойчивость: SAN-кластер обеспечивает резервирование данных и возможность продолжения работы при отказе одного из узлов.
- Масштабируемость: возможность добавления новых узлов кластера для увеличения производительности и расширения хранилища данных.
- Централизованное управление: управление ресурсами и данными в SAN-кластере осуществляется централизованно, что упрощает администрирование и обеспечивает единый доступ к данным.

Задание 2

  Горизонтальный шаринг:
  - Разделение данных по группам пользователей или географическим областям.
  - Создание отдельных баз данных для каждой группы.
  - Например, база данных для пользователей из Европы, Азии и Америки.
    
  Вертикальный шаринг:
  - Разделение данных по типам или категориям.
  - Создание отдельных баз данных для каждой категории данных.
  - Например, база данных для информации о пользователях, книгах и магазинах.
    
  Принципы построения системы:
  - Использование уникальных идентификаторов для связи данных между разными базами.
  - Установка механизмов репликации данных между серверами для синхронизации информации.
  - Разработка единой точки доступа для запросов к разным базам данных.
    
  Разграничение между базами данных:
  - Каждая база данных будет содержать только определенный тип данных (пользователи, книги, магазины).
  - Связи между данными будут поддерживаться через уникальные ключи и внешние ключи.
    
Блоксхема

+-------------------+ 

| Пользователи DB |

+-------------------+

| 

+-------------------+

| Книги DB |

+-------------------+

|

+-------------------+

| Магазины DB |

+-------------------+

Режимы работы серверов:
- Чтение: Различные сервера могут обрабатывать запросы на чтение данных из разных баз данных одновременно.
- Запись: Для операций записи данные могут быть направлены на основной сервер, который будет обновлять все базы данных.





    
