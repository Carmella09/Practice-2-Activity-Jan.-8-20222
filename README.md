# Practice-2-Activity-Jan.-8-20222


(IN PROGRESS)

	#include <iostream>
	#include <string>

	using namespace std;

	int factorial(int n) 
	{
		int c;
		int f = 1;

		for (int c = 1; c <= n; c++) {
			f = f * c;
		}

		return f;
	}
	int main() {
		string name;
		int n;
		cout << "Enter your Full Name: " << endl;
		getline(cin, name);
		cout << "Enter a number between (1-10)" << endl;
		cin >> n;

		while (cin.fail() && n < 1 && n > 10) 
		{
			cin.clear();
			cin.ignore(1000, '\n');
			cout << "Invalid Input";
			cout << "Please try again: ";
			cin.clear();
			cin.ignore();
			cin >> n;
		}
		factorial(n);

		cout << "Factorial of " << n << " is " << factorial(n);
		return 0;
	}




























