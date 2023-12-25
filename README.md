#include <iostream>

using namespace std;

// Abstract base class
class Vehicle {
public:
    // Pure virtual function for movement
    virtual void move() const = 0;
};

// Concrete derived class for a Car
class Car : public Vehicle {
public:
    void move() const override {
        cout << "The car moves on four wheels." << endl;
    }
};

// Concrete derived class for a Bicycle
class Bicycle : public Vehicle {
public:
    void move() const override {
        cout << "The bicycle moves using pedals." << endl;
    }
};

// Concrete derived class for an Airplane
class Airplane : public Vehicle {
public:
    void move() const override {
        cout << "The airplane flies in the sky." << endl;
    }
};

int main() {
    // Using the classes
    Car car;
    Bicycle bicycle;
    Airplane airplane;

    car.move();
    bicycle.move();
    airplane.move();

    return 0;
}
