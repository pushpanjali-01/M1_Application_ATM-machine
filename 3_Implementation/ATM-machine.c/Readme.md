#include<stdio.h><br/>
#include<stdlib.h><br/>
#include<stdbool.h><br/>
#include<math.h><br/>

//Functions<br/>
void login();<br/>
void mainMenu();<br/>
void checkBalance(float balance);<br/>
float moneyDeposit(float balance);<br/>
float moneyWithdraw(float balance);<br/>
void menuExit();<br/>
void errorMessage();<br/>


//Main Code<br/>
int main()<br/> {
    
    int option;
    float balance = 15000.00;
    int choose;

    bool again = true;

    // insert code here...

    while (again) {
    mainMenu();

    printf("=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-\n");
    printf("Your Selection:\t");
    scanf("%d", &option);


        switch (option) {
            case 1:
             system("CLS");
                checkBalance(balance);
                break;
            case 2:
             system("CLS");
                balance = moneyDeposit(balance);
                break;
            case 3:
             system("CLS");
                balance = moneyWithdraw(balance);
                break;

            case 4:
             system("CLS");
                menuExit();
                return 0;

            default:
                errorMessage();
                break;
        }

        printf("=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=\n");
        printf("Would you like to do another transaction:\n");
        printf(" 1: Yes\n");
        printf(" 2: No\n");
        scanf("%d", &choose);

        system("CLS");



        if (choose == 2) {
            again = false;
            menuExit();

        }

}


    return 0;
}//main code



//Functions

void mainMenu() {

    printf("******************Hello!*******************\n");
    printf("**********Welcome to ATM Banking***********\n\n");
    printf("****Please choose one of the options below****\n\n");
    printf("1:Check Balance\n");
    printf("2:Deposit\n");
    printf("3:Withdraw\n");
    printf("4:Exit\n\n");

}//Main Menu

void checkBalance(float balance)<br/> {<br/>
    printf("You Choose to See your Balance\n");<br/>
    printf("\n\n****Your Available Balance is:   $%.2f\n\n", balance);<br/>

}//Check Balance

float moneyDeposit(float balance) <br/>{
    float deposit;<br/>
    printf("You choose to Deposit a money\n");<br/>
    printf("$$$$Your Balance is: $%.2f\n\n", balance);<br>
    printf("****Enter your amount to Deposit\n");<br/>
    scanf("%f", &deposit);<br/>


    balance += deposit;

    printf("\n****Your New Balance is:   $%.2f\n\n", balance);
    return balance;

}//money deposit

float moneyWithdraw(float balance)<br/> {<br/>
    float withdraw;<br/>
    bool back = true;

    printf("You choose to Withdraw a money\n");
    printf("$$$$Your Balance is: $%.2f\n\n", balance);

    while (back) {
    printf("Enter your amount to withdraw:\n");
    scanf("%f", &withdraw);


    if (withdraw && balance) {
        back = false;
        balance -= withdraw;
        printf("\n$$$$Your withdrawing money is:  $%.2f\n", withdraw);
        printf("****Your New Balance is:   $%.2f\n\n", balance);

    }

        else  {

        printf("+++You don't have enough money+++\n");
        printf("Please contact to your Bank Customer Services\n");
        printf("****Your Balance is:   $%.2f\n\n", balance);

    }
    }
    return balance;


}//money withdraw

void menuExit() <br/>{<br/>
    printf("--------------Take your receipt!!!------------------\n");<br/>
    printf("-----Thank you for using ATM Banking Machine!!!-----\n");<br/>
    printf("-----BROUGHT TO YOU BY itsourcecode.com-----\n");<br/>


}//exit menu

void errorMessage() <br/>{<br/>
    printf("+++!!!You selected invalid number!!!+++\n");<br/>
}//error message
