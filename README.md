```c
#include <stdio.h>
int main() {
    int n;
    printf ("Length of the sequence:");
    scanf("%d", &n);

    if (n <= 1 || n >= 10000) {
        return 1;
    }

   
    int dp[n+1];

   
    dp[0] = 1;  
    dp[1] = 2;  
    dp[2] = 4; 

    
    for (int i = 3; i <= n; i++) {
        dp[i] = (dp[i-1] + dp[i-2] + dp[i-3]);
    }

    
    printf("Result:%d\n", dp[n]);

    return 0;
}
