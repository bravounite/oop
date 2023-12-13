#include <iostream>
using namespace std;
#define size 10
int n;
template <class T>
void selection(T A[size])
{
    int i, j, min;
    T temp;
    for (i = 0; i <= n - 2; i++)
    {
        min = i;
        for (j = i + 1; j <= n - 1; j++)
        {
            if (A[j] < A[min])
                min = j;
        }
        temp = A[i];
        A[i] = A[min];
        A[min] = temp;
    }
    cout << "\nSorted list=\n";
    for (i = 0; i < n; i++)
        cout << "\t" << A[i];
}
int main()
{
    int i, A[size];
    float B[size];
    cout << "Selection sort\n";
    cout << "\nInteger Element\n";
    cout << "Enter how many elements you want\n";
    cin >> n;
    cout << "\nEnter the Integer element\n";
    for (i = 0; i < n; i++)
        cin >> A[i];
    selection(A);
    cout << "\nFloat Element\n";
    cout << "Enter how many elements you want\n";
    cin >> n;
    cout << "\nEnter float element\n";
    for (i = 0; i < n; i++)
        cin >> B[i];
    selection(B);
    return 0;
}
