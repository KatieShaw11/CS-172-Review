//CS-172-Review
=============

//CS-172 Review Homework
//
// Katie Shaw
// CS172 Review
// May 21
//

#include <iostream>
#include <cmath>
#include <cstdlib>
#include <ctime>
#include <string>
#include <stdio.h>      /* printf, scanf, puts, NULL */
#include <stdlib.h>     /* srand, rand */
#include <time.h>
using namespace std;

void ex02 ();
void ex03();
void ex04();
void doubleNum (int Num);
int add (int A, int B);
void addOne (int & passBy);
void ex05();
void array1(int Array[], int I);
void array2(int Array[], int I);



int main()
{
    ex02();
    ex03();
    ex04();
    ex05();
    
}


void ex02()
{
    cout << "*****EX02******\n\n";
    // (a)
    bool hasPassedTest = 1;
    cout << "\n\nA:\n\n" << "Variable hasPassedTest = 1 (true)\n\n";
    
    // (b)
    cout << "\n\nB:\n\n";
    int x = rand() % 100;
    int y = rand() % 100;
    
    if (x>y)
        cout << "X (" << x << ") is greater than y (" << y << ").\n";
    else if (y>x)
        cout << "Y (" << y << ") is greater than x (" << x << ").\n";
    else if (x == y)
        cout << "X and y are the same.\n";
    
    // (c)
    cout << "\n\nC:\n\n";
    
    int numberOfShares;
    cout << "Type in a value:\n";
    cin >> numberOfShares;
    if (numberOfShares < 100)
        cout << numberOfShares << " is less than 100.\n";
    else if (numberOfShares > 100)
        cout << numberOfShares << " is greater than 100.\n";
    else if (numberOfShares == 100)
        cout << numberOfShares << ", the number you entered, is 100!\n";
    
    // (d)
    cout << "\n\nD:\n\n";

    int box;
    int book;
    
    cout << "What is a box width? What is book width?";
    cin >> box;
    cin >> book;
    
    if (box%book == 0)
        cout << "The box width is evenly divisible by the book width.\n\n";
    else
        cout << "The box width is NOT evenly divisible by the book width.\n\n";

    
    // (e)
    cout << "\n\nE:\n\n";
    
    int shelfLife;
    int temp;
    
    cout << "What is the shelf life of the chocolate? What is the outside temperature?\n";
    cin >> shelfLife;
    cin >> temp;
    
    if (temp > 90)
    {
        shelfLife -= 4;
        cout << "Actually, since the temperature is so high, the shelf life is " << shelfLife << endl << endl;
    }
    
}

void ex03()
{
    cout << "\n\n*****EX03******\n\n";

    // (a)
    cout << "\n\nA:\n\n";

    float area;
    float a; // sides of square
    float c; // diagonal (hypotenuse)  (c^2 = 2a^2)
    float power = 2.0;
    
    cout << "What is the area of the square?\n";
    cin >> area;
    
    a = sqrt(area);
    
    c = sqrt(2 * (pow(a,power)));
    
    cout << "The diagonal of the square is " << c << ".\n";
    
    // (b)
    cout << "\n\nB:\n\n";

    char response;
    
    cout << "Yes or no? (y/n)\n";
    cin >> response;
    
    if (response == 'y')
        cout << "Yes!\n";
    else if (response == 'n')
        cout << "Nooooooo.\n";
    
    // (c)
    cout << "\n\nC:\n\n";
    
    char tab = '\t';
    
    cout << "Variable tab is equal to a tab.";
    
    // (e)
    cout << "\n\nE:\n\n";
    
    string mailingAddress = ""; // (e)
    
    cout << "At this point, \"mailingAddress\" is initialized as an empty string.";
    
    // (d)

    cout << "\n\nD:\n\n";
    
    cout << "What is your mailing address?\n";
    
    getline (cin, mailingAddress);
    
    cout << "Mailing address: " << mailingAddress << ".";
}

void ex04()
{
    cout << "\n\n*****EX04******\n\n";

    // (a)
    cout << "\n\nA:\n\n";
    
    int num = 11;
    
    while(num > 10 || num < 1)
    {
        cout << "\nGive us a number between one and ten.\n";
        cin >> num;
    }
    
    // (b)
    cout << "\n\nB:\n\n";
    int bsum=0;
    
    for (int i = 1; i <= num; i++)
    {
        bsum = bsum + (i*i*i);
    }
    
    cout << "The sum of the cubes is: " << bsum << ".";
    
    // (c)
    cout << "\n\nC:\n\n";
    
    int count = 0;
    do {
        cout << "*";
        count++;
    }
    while(count < num);
    
    
    // (d)
    cout << "\n\nD:\n\n";
    
    cout << "\n\nEven numbers from 0 to 40 are: ";
    for (int i = 0; i < 41; i++)
    {
        if (i%2==0)
            cout << i << " ";
    }
    
    // (e)
    cout << "\n\nE:\n\n";
    
    doubleNum(num);
    
    // (f)
    cout << "\n\nF:\n\n";
    
    int a = rand()%100;
    int b = rand()%100;
    int sum = add(a, b);
    cout << "\nSum is: " << sum << ".\n";
    
    // (g)
    cout << "\n\nG:\n\n";
    
    addOne (num);
    cout << "That old number plus one is " << num << ".";

    
}

void doubleNum (int Num) // (e)
{
    Num = Num*2;
    cout << "Double the input is " << Num << ".";
}

int add (int A, int B)
{
    return A + B;
}

void addOne (int & passBy)
{
    passBy++;
}


void ex05()
{
    cout << "\n\n*****EX05******\n\n";

    // (a)
    cout << "\n\nA:\n\n";
    
    int iSize = 5;
    int arr[iSize];
    
    for (int i = 0; i < 5; i++)
    {
        cout << "Please input an integer:\n";
        cin >> arr[i];
    }
    
    // (b)
    cout << "\n\nB:\n\n";
    
    int sum = 0;
    int prod = 1;
    
    for (int i = 0; i< 5; i++)
    {
        sum = sum + arr[i];
        prod = prod * arr[i];
    }
    
    cout << "The sum of these integers is " << sum << ".\n";
    cout << "The product of these integers is " << prod << ".\n";
    
    // (c)
    cout << "\n\nC:\n\n";
    
    array1(arr, iSize);
    
    // (d)
    cout << "\n\nD:\n\n";
    
    array2(arr, iSize);

    
}

void array1(int Array[], int I) // (c)
{
    cout << "Ex05: C:\n";
    for (int i = 0; i < I; i++)
    {
        cout << "Array[" << i << "]: " << Array[i] << endl;
    }
}

void array2(int Array[], int I) // (d)
{
    int input;
    cout << "\nPlease input a value: \n";
    cin >> input;
    bool check = 0;
    
    for (int i = 0; i < I; i++)
    {
        if (Array[i] == input)
        {
            cout << "This value (" <<input<< ") is equal to element number " << i+1 << " in the array.\n";
            check = 1;
        }
    }
    if (check == 0)
        cout << "None of the array elements equal this number.";
}




