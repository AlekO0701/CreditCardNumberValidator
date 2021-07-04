# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

03.11.2020 г. - 03.11.2020 г. было проведено функциональное тестирование приложения Credit Card Number Validator.

На тестирование затрачено: 1 час 30 мин.

В результате тестирования выявлены следующие дефекты:
* при введении в приложение Credit Card Number Validator номеров карт состоящих из 15 и менее цифровых символов, приложение выдает сообщенте FAIL;
* при введении в приложение Credit Card Number Validator номеров карт состоящих из 17 и более цифровых символов, приложение выдает сообщенте FAIL;

## Описание процесса тестирования

В качестве тестовых данных использовал генератор валидных номеров кредитных карт:
1. Открыть [генератор](https://www.freeformatter.com/credit-card-number-generator-validator.html)
2. Копировать номер карты из любого столбца;
3. Запустить проект Credit Card Number Validator В среде IntelliJ IDEA Community:
4. В 4-ой строке проекта String number = "<вствить номер карты>";
5. Нажать сочетание клавиш на клавиатуре Shift+F10;
6. Ожидаемый результат - в окне Run появится сообщение "Result is OK".  

## Тестирование производилось в следующем окружении:
* Windows 10, 64-разрядная операционная система

* версия JDK "11.0.9" 2020-10-20

* версия IntelliJ IDEA 2020.2.3 (Community Edition)
Build #IC-202.7660.26, built on October 6, 2020
Runtime version: 11.0.8+10-b944.34 amd64
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.
Windows 10 10.0
GC: ParNew, ConcurrentMarkSweep
Memory: 858M
Cores: 8

* Google Chrom Версия 86.0.4240.111 (Официальная сборка), (64 бит)