## Prime number

You are given an integer N. You need to print the series of all prime numbers till N.

#### Input Format

The first and only line of the input contains a single integer N denoting the number till where you need to find the series of prime number.

#### Output Format

Print the desired output in single line separated by spaces.
```
Constraints

1<=N<=1000
```
#### Solution:
```go
package main

import "fmt"

func isPrime(n int) bool {
    if n<=1 {
        return false;
    }
    
    if n<=3 {
        return true;
    }
    
    if n%2 == 0 || n%3 == 0 {
        return false;
    }
    
    //var i int;
    for i:=5; i*i<=n; i=i+6{
        if n%i == 0 || n%(i+2) ==0{
            return false;
        }
    }
    return true;
}

func printPrime(n int){
    //function to print the prime numbers
    //var a int;
    for a:=2;a<n;a++ {
        if isPrime(a) {
            fmt.Printf("%d ",a);
        }
    }
}

func main(){
    var n int;
    fmt.Scanf("%d", &n);
    printPrime(n);
}
```
