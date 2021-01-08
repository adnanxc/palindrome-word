# palindrome-word
 Write a function that takes a string as a parameter and check the string is a palindrome or not palindrome. Then returns the result to the main function.


#include <iostream>
using namespace std;

int pchecker(string s){
    int length , isPalindrome=1;
    length = s.length();

    for(int i=0; i<length; i++){
        if(s[i] != s[length-1-i]){
            isPalindrome = 0;
            break;
        }
    }
    return isPalindrome;
}

int main(){

    string a;
    cout << "Enter the string: ";
    cin >> a;
    int x = pchecker(a);
    if(x==1){
        cout << "Palindrome";
    }
    else {
        cout << "Not a palindrome";
    }
    return 0;
}
