# pt3
#include <iostream>
#include <fstream>
using namespace std;
int main (){
    string name;
    int n, range;
    ifstream fin;
    ofstream fout;
    char ch;
    fin.open("pt3.txt");
    fout.open("pt3.txt");

    do{
        cout << "Enter range of numbers: ";
        fout << "Enter range of numbers: ";
        cin >> range;
        fin >> range;
        for (int n, count = 1; count <= range; count++){
            cout << "Enter number " << "[" << count << "]: ";
            fout << "Enter number " << "[" << count << "]: ";
            cin >> n;
            fin >> n;
            if (n % 2 == 0){
            cout << n << " is an EVEN number." << endl;
            fout << n << " is an EVEN number." << endl;
            } else {
            cout << n << " is an ODD number." << endl;
            fout << n << " is an ODD number." << endl;
            }
        }
            cout << "Try again [y/n]: ";
            fout << "Try again [y/n]: ";
            cin >> ch;
            fin >> ch;
            cout << endl;
    } while (ch == 'y');

    fin.close();
    return 0;
}
