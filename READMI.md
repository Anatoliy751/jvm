public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1
        Object o = new Object();        // 2
        Integer ii = 2;                 // 3
        printAll(o, i, ii);             // 4
        System.out.println("finished"); // 7
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5
        System.out.println(o.toString() + i + ii);  // 6
    }
}

класс JvmComprehension загружается всю информацию в область памяти ,
проверяется весь код на его ошибки в режиме онлайн.
после начинается работа с методом main, когда вызывается метод мейн, он же создается в памяти фрейм, а та в свою очередь  создается в стэке 
после чего (1) создается примитивный тип данных в стеке
дальше (2) строка это ссылочный тип данных хранится в стеке. в стеке сохранается объект типа о в которую сохраняется новыц объект
строка (3) класс интегжер создается класс в хипи. ссылка на объект в памяти передается в переменную ии
(4) вызывается метод принталл в котором лежат три переменные которые были созданы
(7) выводит на экран пользователя данные
(5) создаем переменную ссылочную, в хипи создается объект итегжер со значением принт алл
в стеке во фрейме принталл создается переменная юзливар
(6) вызывается метод принтлн который есть у объекта оут- находится в классе систем, который создает метод фрейм. туда передаются значения в скобках, сводятся до одного значения и передаются в метод принтлн
метод завершается фрейм закрывается после чего в первый фрейм создается еще один фрейм обрабатывается и выводит результат после чего программа завершает свою работу и приступает к работе сборщик мусора который определяет какие объекты используются а какие нет
