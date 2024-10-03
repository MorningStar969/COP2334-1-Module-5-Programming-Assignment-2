# COP2334-1-Module-5-Programming-Assignment-2
This is a GitHub repository link for the second Programming Assignment from Module 5.

// This program is created to calculate the total occupancy rate of a hotel by totalling the number of rooms that are occupied and dividing it by the total number of rooms in the hotel.

// Header Files
#include <iostream>
using namespace std;
// Main Function
int main() {
  // Declaring Variables
  int floors, totalRooms = 0, totalOccupied = 0;
  cout << "Enter the number of floors in the hotel: ";
  cin >> floors;
  // Loop to iterate through each floor
  for (int i = 1; i <= floors; i++) {
    int rooms, occupied;
    cout << "Enter the number of rooms on floor " << i << ": ";
    cin >> rooms;
    // Loop to iterate through each room on the floor
    cout << "Enter the number of occupied rooms on floor " << i << ": ";
    // Input Validation
    cin >> occupied;
    totalRooms += rooms;
    totalOccupied += occupied;
  }
  // Output
  int unoccupied = totalRooms - totalOccupied;
  double occupancyRate = (double)totalOccupied / totalRooms;
  cout << "Total rooms: " << totalRooms << endl;
  cout << "Total occupied rooms: " << totalOccupied << endl;
  cout << "Total unoccupied rooms: " << unoccupied << endl;
  cout << "Occupancy rate: " << occupancyRate << endl;
  return 0;
}
