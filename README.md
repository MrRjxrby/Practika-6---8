#6 практическая задание 3
```
public class Main {
    interface Nameable {
        String getName();
    }

    static class Planet implements Nameable {
        private String name;

        public Planet(String name) {
            this.name = name;
        }

        @Override
        public String getName() {
            return name;
        }
    }

    static class Car implements Nameable {
        private String name;

        public Car(String name) {
            this.name = name;
        }

        @Override
        public String getName() {
            return name;
        }
    }

    static class Animal implements Nameable {
        private String name;

        public Animal(String name) {
            this.name = name;
        }

        @Override
        public String getName() {
            return name;
        }
    }

    public static void main(String[] args) {
        Planet earth = new Planet("Земля");
        Car myCar = new Car("Audi A3");
        Animal cat = new Animal("Рыжий");

        System.out.println("Имя планеты: " + earth.getName());
        System.out.println("Название машины: " + myCar.getName());
        System.out.println("Кличка Кота: " + cat.getName());
    }
}
```
# 7 практика 4 задание
```
public class Main {
    interface MathCalculable 
{
        double PI = 3.14159265358979323846;

        ComplexNumber pow(ComplexNumber base, int exponent);

        double abs(ComplexNumber number);
    }

    static class ComplexNumber {
        double real;
        double imaginary;

        public ComplexNumber(double real, double imaginary) {
            this.real = real;
            this.imaginary = imaginary;
        }

        @Override
        public String toString() {
            return "(" + real + " + " + imaginary + "i)";
        }
    }

    // Класс MathFunc
    static class MathFunc implements MathCalculable {

        @Override
        public ComplexNumber pow(ComplexNumber base, int exponent) {
            double r = Math.sqrt(base.real * base.real + base.imaginary * base.imaginary);
            double theta = Math.atan2(base.imaginary, base.real); 

            double newR = Math.pow(r, exponent);
            double newTheta = exponent * theta;

            double newReal = newR * Math.cos(newTheta);
            double newImaginary = newR * Math.sin(newTheta);

            return new ComplexNumber(newReal, newImaginary);
        }

        @Override
        public double abs(ComplexNumber number) {
            return Math.sqrt(number.real * number.real + number.imaginary * number.imaginary);
        }

        public double calculateCircumference(double radius) {
            return 2 * PI * radius;
        }
    }

    public static void main(String[] args) {
        MathFunc mathFunc = new MathFunc();

        ComplexNumber complexNumber = new ComplexNumber(1, 1);
        ComplexNumber resultPow = mathFunc.pow(complexNumber, 2); 
        double resultAbs = mathFunc.abs(complexNumber); 

        double circumference = mathFunc.calculateCircumference(5); 

        System.out.println("Результат возведения в квадрат: " + resultPow);
        System.out.println("Результат модуля: " + resultAbs);
        System.out.println("Результат длины окружности: " + circumference);
    }
}
```
# 8 практика задание 11
```
import java.util.Scanner;

public class CountOnes {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int count = 0;
        int previous = -1; 
        
        while (true) {
            int number = scanner.nextInt();
            
            if (number == 0 && previous == 0) {
                break; 
            }
            
            if (number == 1) {
                count++;
            }
            
            previous = number;
        }
        
        System.out.println("Количество единиц: " + count);
    }
}
```
# Задание 12
```
import java.util.ArrayList;
import java.util.Scanner;

public class Main {
    public static void OddNumbers() {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Integer> Numbers = new ArrayList<>(); 

        while (true) {
            int number = scanner.nextInt();

            if (number == 0) {
                break; 
            }

            if (number % 2 != 0) { 
                Numbers.add(number); 
            }
        }

        for (int number : Numbers) {
            System.out.println(number);
        }
    }

    public static void main(String[] args) {
        OddNumbers(); 
    }
}
```
# Задание 13
```
import java.util.Scanner;
import java.util.ArrayList;

public class Main {
        public static void OddNumbers() {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Integer> Numbers = new ArrayList<>(); 
        int i = 1; 

        while (true) {
            int number = scanner.nextInt(); 

            if (number == 0) {
                break; 
            }

            if (i % 2 != 0) { 
                Numbers.add(number); 
            }

            i++; 
        }
        for (int number : Numbers)
        {
            System.out.println(number);
        }
    }

    public static void main(String[] args) {
        OddNumbers(); 
    }
}
```
