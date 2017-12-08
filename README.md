# improved-octo-doodle
Just another repository

#include<stdio.h>
#define MOD 1000000007
// a^x
unsigned long long pow(unsigned long long a,
                       unsigned long long x)
{
    unsigned long long result=1;
    a%=MOD;
    while(x)
    {
        if(x&1)
            result=(result*a)%MOD;
        a=(a*a)%MOD;
        x>>=1;
    }
    return result;
}

int main()
{
    freopen("C:\\temp\\test.txt","r",stdin);
    unsigned long long a,x;
    scanf("%llu%llu",&a,&x);
    printf("%llu\n",pow(a,x));
    return 0;
}
