# 05-virt-01-basics
Homework
1.Опишите кратко, в чём основное отличие полной (аппаратной) виртуализации, паравиртуализации и виртуализации на основе ОС.
 
 Полная (аппаратная) виртуализация создает образ физического хоста, тем самым, полностью изолируя гостевую ОС.

 Паравиртуализация использует гостевые ОС под управлением гипервизора, использует аппаратные ресурсы физического хоста.
 
 Виртуализация уровня ОС происходит на уровне ядра пользовательско ОС, соответственно использовать в контейнерах приложения на базе ОС другого ядра невозможно

2. Выберите один из вариантов использования организации физических серверов в зависимости от условий использования.
   Организация серверов:

    физические сервера,
    паравиртуализация,
    виртуализация уровня ОС.

Условия использования:

    высоконагруженная база данных, чувствительная к отказу;
    различные web-приложения;
    Windows-системы для использования бухгалтерским отделом;
    системы, выполняющие высокопроизводительные расчёты на GPU.

Опишите, почему вы выбрали к каждому целевому использованию такую организацию.

Ответ:
    Высоконагруженная база данных, чувствительная к отказу - может использоваться физический сервер для поддержания высокого уровня производитедьности, возможно также использование оптимизированных паравиртуализированных решений с увеличиеним производительности и соответственно стоимости.

    Различные web-прилодения - возможно использлвание виртуализации уровня ОС для удобства и простоты тестирования и развертывания приложений.

    Windows-системы для использования бухгалтерским отделом - использование паравиртуализации для удобного бэкапирования и поддержки устаревших ОС на более мощных ресурсах.

    Системы, выполняющие высокопроизводительные расчёты на GPU - использование физических серверов для высокого уровня производительности.

  3. Выберите подходящую систему управления виртуализацией для предложенного сценария. Детально опишите ваш выбор.

Сценарии:

    1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
    2. Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
    3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
    4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.

Ответ:

    1. VMWare ESXI или Hyper-V в данном случае подойдут по функционалу. Учитывая преимущественность Windows based инфраструктуры возможно Hyper-V подойдёт большей ввиду лучшей совместимости.


2. Могут подойти Xen, KVM или Proxmox VE в зависимости от выполняемых операций.


3. Microsoft Hyper-V Server имеющий наибольшую совместимость с Windows системами или как альтернатива Xen


4. Наибольшую скорость развёртывания обеспечивают решения виртуализации уровне ОС по типу Docker

  4. Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет? Мотивируйте ваш ответ примерами.

     Проблемы:

Высокий уровень квалификации персонала по управлению разнородными ПО виртуализации.



Высокие расходы на проприетарные системы управления виртуализацией.


Сложность переноса виртуальных машин между различными средами и масштабирование

Гетерогенная среда виртуализации представляет собой достаточно сложную систему управления виртуализацией в части высокого уровня компетенции.
Возможно использовать полную и виртуализацию на уровне ОС для распределения аппаратных ресурсов при выполнении задач по развертиванию ПО.


