# random_numbers
The program generates 10000 random numbers and saves it in the text file

#include <iostream>
#include <cstdlib>
#include <fstream>

int main() {
	std::ofstream output;
	output.open("RandomNumbers.txt");
	
	int random = 0;
	srand(time(0));
	for (int i = 0; i < 10000; i++) {
		random = rand();
		output << random << " \n";
	}
	
	output.close();
	return 0;
}
