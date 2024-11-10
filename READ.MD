# 6 практическая, задание 3
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
