# Function
include <stdio.h>

    void print_menu();
    long fact(int);
    int nCr(int,int);
    int sum(int);
    
int main(int argc, const char * argv[]) {
int menu;
int n,r;

    do{
    print_menu();
    scanf("%d",&menu);
        if(menu<4){
        printf("Input your number(n): ");
        scanf("%d",&n);
        }

    switch (menu) {
    case 1: printf("Your factorial (%d!) is %ld\n",n, fact(n));
    break;

    case 2: printf("Input your \'r\'");
    scanf("%d",&r);
    printf("Your %dC%d is %d\n", n,r,nCr(n,r));
    break;

    case 3: printf("Your sumation(Sum(n)) is %d\n", sum(n));
    break;

    default:
    break;
    } 
        
    } while(menu<4);

}

    void print_menu(){
        printf("Your choices is ");
    }

    long fact(int n){
        long f;
        for(f=1;n>=1;n--){
            f*=n;
            }
            return f;
    }
    
    int nCr(int n, int r) {
    long h=1, l=1, nCr;
    int i,j,k;

    for(i=1;i<=n;i++){
        h*=i;
    }
    for(j=1;j<=r;j++){
        l*=j;
    }
    int in=n-r;
    for(k=1;k<=in;k++){
        l*=k;
    }

    nCr=h/l;
    return nCr;
    }

    int sum(int x){
        int s;
        for(s=0;x>0;x--){
            s+=x;
        }
        return s;
    }
    
