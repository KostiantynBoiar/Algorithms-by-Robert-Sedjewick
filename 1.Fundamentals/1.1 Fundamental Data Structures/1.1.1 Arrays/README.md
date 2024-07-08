# Arrays

Perhaps the most fundamental data structure is the **array**, which is defined as a primitive in C and most other programming languages.

Array
: is a fixed number of data items that are sotred contiguously and that are accesible by an index.

We refer to the *i*th element of an array *a* as *a[i]*. A simple example of use of an array is given by the following program, which prints out all the prime number less than 1000. The method used, which dates back to the 3rd century B.C, is called the "sieve of Eratosthenes"
```C

#define N 1000
main(){
  int i, j, a[N+1];
  for(a[1] = 0, i = 2; i <= N; i++) a[i] = 1;
  for(i = 2; i <= N/2; i++)
    for(j = 2; j <= N/i; j++) a[i*j] = 0;
  for(i = 1; i <= N; i++)
    if(a[i]) printf("%4d", i);
  printf("\n");
}

```


