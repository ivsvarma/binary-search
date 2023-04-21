# binary-search
Binary Search is defined as a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(log N). 


#include <iostream>

using namespace std;

int main()
{


    int n,i,a,low,high,mid;
    cout<<"enter the no.of element";
    cin>>n;
    int arr[n];
    cout<<"enter the element in sorted way";
    for (i=0;i<n;i++)
    cin>>arr[i];
    cout<<"enter the element to be search";
    cin>>a;
    low=0;
    high=n-1;
    mid=(low+high)/2;
    while(low<=high){
        if(arr[mid]<a)
        low=mid+1;
        else if(arr[mid]==a){
        cout<<a;
        break;
        }
        else {
        high=mid-1;
        mid=(low+high)/2;
        }
        if(low>high)
        cout<<"not present";




    }

    return 0;
}
