#include <iostream>
using namespace std;

class Animal {
public:
    virtual void makeSound() = 0;
};

class Dog : public Animal {
public:
    void makeSound() {
        cout << "멍멍" << endl;
    }
};

class Cat : public Animal {
public:
    void makeSound() {
        cout << "야옹" << endl;
    }
};

class Cow : public Animal {
public:
    void makeSound() {
        cout << "음메" << endl;
    }
};

int main() {

    Animal* animals[3];

    Dog dog;
    Cat cat;
    Cow cow;

    animals[0] = &dog;
    animals[1] = &cat;
    animals[2] = &cow;

    for (int i = 0; i < 3; ++i) {
        animals[i]->makeSound();
    }

    return 0;
}
