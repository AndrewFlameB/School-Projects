# School-Projects

#include <iostream>
using namespace std;

class TowersofHanoi {
  public:
  // takes in 4 int values, the amount of circles and names for sticks
  // usescout to cout to print everything out
    void tower(int x, int Stick1, int Stick2, int Stick3) {
    if(x == 1) {
        std::string stickThingy = "Move disk from stick " + std::to_string(Stick1) + " to stick " + std::to_string(Stick3) + "\n";
        cout << stickThingy;
    } else {
        // uses a pattern to dissasemble and reassemble tower
        tower(x-1, Stick1, Stick3, Stick2);
        std::string stickThingy = "Move disk from stick " + std::to_string(Stick1) + " to stick " + std::to_string(Stick3) + "\n";
        cout << stickThingy;
        tower(x-1, Stick2, Stick1, Stick3);
    }
    }
};

int main() {
  TowersofHanoi myObj;
  myObj.tower(4, 1, 2, 3);
  return 0;
}
