# Spiral-matrix
problem solving
<br> <br>
#include<iostream>
using namespace std;
int main() {
    int arr[4][4] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16};
    int n = sizeof(arr) / sizeof(arr[0]); // rows
    int m = sizeof(arr[0]) / sizeof(arr[0][0]); // columns
    int strow = 0, stcol = 0, endrow =  m - 1, endcol = n-1;
    while(strow <= endrow && stcol <= endcol) {
        // top
        for(int i=stcol;i<=endcol;i++) {
            cout<<arr[strow][i]<<" ";
        } 
        //right
        for(int j = strow+1; j <= endrow;j++) {
            cout<<arr[j][endcol]<<" ";
        } 
        // bottom 
        for(int i = endcol-1;i >=stcol;i--) {
            cout<<arr[endrow][i]<<" ";
        } 
        // left
        for(int j=endrow-1;j>=endrow+1;j--) {
            cout<<arr[j][stcol]<<" ";
        }
        strow++ , stcol++, endrow-- , endcol--;
    }
    return 0;
}
