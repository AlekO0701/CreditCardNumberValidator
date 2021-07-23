Легенда
Вы попали в небольшой стартап, который помогает осуществлять приём платежей с банковских карт различным организациям.

Стартап находится в самом этапе зарождения, поэтому первое, что они решили сделать - реализовать функциональность валидации номера банковской карты.

Но как всегда бывает в стартапах, программист, который взялся реализовывать эту функциональность, исчез и не отвечает на звонки.

Но от него остались некоторые наработки вот в таком виде:

public class Main {

  public static void main(String[] args) {
  
    // TODO: подставлять номер карты нужно сюда между двойными кавычками, без пробелов
    String number = "5351719427810741";
    System.out.println(String.format("Result is %s", isValidCardNumber(number) ? "OK" : "FAIL"));
  }

  public static boolean isValidCardNumber(String number) {
    if (number == null) {
      return false;
    }

    if (number.length() != 16) {
      return false;
    }

    long result = 0;
    for (int i = 0; i < number.length(); i++) {
      int digit;
      try {
        digit = Integer.parseInt(number.charAt(i) + "");
      } catch (NumberFormatException e) {
        return false;
      }

      if (i % 2 == 0) {
        digit *= 2;
        if (digit > 9) {
          digit -= 9;
        }
      }
      result += digit;
    }

    return (result != 0) && (result % 10 == 0);
  }
}

Что вам нужно сделать:

Установить IntelliJ IDEA согласно Руководство по установке IntelliJ IDEA
Проверить работу этой программы (нужно заменить код с "Hello programming!" целиком на тот, что приведён выше) и запускать программу с разными тестовыми данными (запуск описан в п. "Шаг 20" Руководства по установке IntelliJ IDEA)
Подготовьте отчёт о проведённом тестировании в указанном формате и разместите его в репозитории. Инструменты форматирования текста в .md-файлах вы можете найти здесь или открыть шаблон и нажать на кнопочку Raw справа сверху.
Важно: вам не нужно разбираться в самом коде и пытаться его понять, вам нужно лишь научиться его запускать и менять номер карты на 4-ой строке.

Важно: внимательно следите за тем, чтобы в отчёты не попадали реальные номера карт (на данный момент* это неприемлимая практика тестировать на собственных данных: персональных, платёжных и других).
