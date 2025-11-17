# Coffeeapi
api for coffee.alexflipnote.dev random coffee images generator
# main
```cpp
#include "Coffeeapi.h"
#include <iostream>

int main() {
   Coffeeapi api;

    auto coffee = api.get_random_coffee().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    coffee.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
