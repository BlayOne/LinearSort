
#include<iostream>

using namespace std;

int LinearSearch(int arr[], int num, int size)
{
if(size == 0) return -1; else if( num == arr[size-1]) return size; else
return LinearSearch(arr,num,size-1);
}

int main()
{ int Arr[20],length,iKey;
int i,Position = 0;
cout << "\nEnter array size\n";
cin>>length;
cout << "\nEnter array elements:\n";
for(i = 0; i < length; i++){
cin>>Arr[i];
}
cout << "\nenter the key element\n"; 
cin >> iKey;
Position = LinearSearch(Arr,iKey,length);
if(Position == -1){
    cout<< "\nElement unavailable\n"; 
}else {
    cout<< "\nElement available at position " << Position<<endl;
}
return 0;
}
