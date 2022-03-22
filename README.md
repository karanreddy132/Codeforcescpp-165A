# Codeforcescpp-165A
#include <bits/stdc++.h>

using namespace std;

int main()
{
  int n,x[1001],y[1001],left(0),right(0),top(0),bottom(0),count(0),c(0);
  cin >> n;
  for(int i=0;i<n;i++){
    cin >> x[i] >> y[i];
  }
  for(int i=0;i<n;i++){
    left = 0;
    right = 0;
    top = 0;
    bottom = 0;
    count = 0;
    for(int j=0;j<n;j++){
      if((x[i] > x[j] && y[i]==y[j]) && left==0){
        count++;
        left = 1;
      }
      else if((x[i] < x[j] && y[i]==y[j]) && right==0){
        count++;
        right = 1;
      }
      else if((y[i] > y[j] && x[i]==x[j]) && bottom==0){
        count++;
        bottom = 1;
      }
      else if((y[i] < y[j] && x[i]==x[j]) && top==0){
        count++;
        top = 1;
      }
      if(count==4){
        c++;
        break;
      }
    }
  }
  cout << c;
  return 0;
}
