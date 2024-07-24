#include <iostream>
#include <map>
#include <set>
using namespace std;

// Class representing a User
class User {
public:
    string firstName;
    string lastName;
    int age;
    string gender;

    User() {}
    User(string firstName, string lastName, int age, string gender) {
        this->firstName = firstName;
        this->lastName = lastName;
        this->age = age;
        this->gender = gender;
    }
};

// Global maps for users and friendships
map<string, User> mapUserName;
map<string, set<string>> Friends;

// Function to add a user
void addUser(string userName, User user) {
    if (mapUserName.find(userName) == mapUserName.end()) {
        mapUserName[userName] = user;
        cout << "User added successfully: " << userName << endl;
    } else {
        cout << "UserName Already Taken" << endl;
    }
}

// Function to make two users friends
void makeThemFriend(string userName1, string userName2) {
    Friends[userName1].insert(userName2);
    Friends[userName2].insert(userName1);
    cout << userName1 << " and " << userName2 << " are now friends." << endl;
}

// Function to display all registered users
void displayAllUsers() {
    cout << "All Registered Users:\n";
    for (auto& user : mapUserName) {
        cout << "UserName: " << user.first << ", Name: " << user.second.firstName << " " << user.second.lastName << endl;
    }
}

// Function to display all friendships
void displayAllFriendships() {
    cout << "All Friendships:\n";
    for (auto& pair : Friends) {
        cout << pair.first << " -> ";
        for (auto& friendName : pair.second) {
            cout << friendName << " ";
        }
        cout << endl;
    }
}

int main() {
    // Creating users
    User alice("Alice", "Mishra", 30, "Female");
    User bob("Bob", "Ali", 27, "Male");

    // Adding users to the system
    addUser("Alice", alice);
    addUser("Bob", bob);

    // Making Alice and Bob friends
    makeThemFriend("Alice", "Bob");

    // Displaying all registered users and friendships
    displayAllUsers();
    displayAllFriendships();

    return 0;
}
