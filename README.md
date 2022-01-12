# Sieve-of-Eratothenes
#include <bits/stdc++.h>


using namespace std;

void MarkingPrimes(int n){
    //Make array of booleans

  bool primes[n + 1];
    memset(primes, true, sizeof(primes));
    for(int i=2; i*i<=n;i++){
        if(primes[i]==1){
            for(int j=i+i;j<=n;j=j+i){
                primes[j]=0;
            }
        }
    }
    for(int i=0;i<n;i++){
        if(primes[i]==1){
            cout<<i<<" ";
        }
    }
}


int main()
{
    int i=87;
    MarkingPrimes(i);
    return 0;
}
