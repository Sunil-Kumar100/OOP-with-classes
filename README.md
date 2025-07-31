# OOP-with-classes
public class Main {
    // Base class
    static class Vehicle {
        String brand;
    // Constructor
        Vehicle(String brand) {
            this.brand = brand;
        }
    // Method to be overridden
        void start() {
            System.out.println(brand + " vehicle is starting.");
        }
        void stop() {
            System.out.println(brand + " vehicle is stopping.");
        }
    }
    // Derived class 1
    static class Car extends Vehicle {
        Car(String brand) {
            super(brand);
        }
    // Overriding start method
        @Override
        void start() {
            System.out.println(brand + " car is starting with a key ignition.");
        }
    }
    // Derived class 2
    static class Bike extends Vehicle {
        Bike(String brand) {
            super(brand);
        }
    // Overriding start method
        @Override
        void start() {
            System.out.println(brand + " bike is starting with a kick.");
        }
    }
    // Main method
    public static void main(String[] args) {
          Vehicle vehicle = new Vehicle("Generic");
          Car car = new Car("Honda");
          Bike bike = new Bike("Royal Enfield");
        System.out.println("== Vehicle ==");
        vehicle.start();
        vehicle.stop();
          System.out.println("\n== Car ==");
          car.start();
          car.stop();
        System.out.println("\n== Bike ==");
        bike.start();
        bike.stop();
    }
}
