#include<bits/stdc++.h>          // incomplete
using namespace std;

// partition sort - divide and conquer algorithm  (a recursive algo )

// helper method
int partition(vector<int> &arr,int s,int e){
    int i=s; // ptr at begn of 1st half
    int m=(s+e)/2;
    int j=m+1;  // ptr at begn of 2nd half(partition)

    vector<int> temp;
    while(i<=m and j<=e){
        if(arr[i]<arr[j]){
            temp.push_back(arr[i]);
            i++;
        }
        else{
            temp.push_back(arr[j]);
            j++;
        }
    }
    // this loop will break when any 1 half of the arr is exhausted

    //so copy rem elems from 1st half
    while(i<=m){
        temp.push_back(arr[i++]);
    }
    //so copy rem elems from 2nd half
    while(j<=e){
        temp.push_back(arr[j++]);
    }

    // copy back the elements from temp to orig arr
    int k=0;
    for(int idx=s; idx<=e;idx++){
        arr[idx]=temp[k++];
    }
    return ;
}

// sorting method
int quicksort(vector<int> &arr,int s,int e){  //s-start(idx)|e-end(idx)
    //base case
    if(s>=e){  // i.e it has 1 or 0 elements
        return;
    }
    //recursive case
    int p=partition(arr,s,e);
    
}

int main(){ios_base::sync_with_stdio(false); cin.tie(0);

    vector<int> arr{10,5,2,0,7,6,40,-8};
    int s=0,e=arr.size()-1;
    quicksort(arr,s,e);
    for(int x: arr){
        cout<<x<<',';
    }
    cout<<endl;
    
return 0;
}
