#include "unity.h"<br/>
#include <ATM-machine.h>


#include <ATM-machine.h><br/>
#define PROJECT_NAME    "ATM-machine"<br/>




void test_login(void);<br/>
void test_checkBalance(float balance);<br/>
float test_moneyDeposit(float balance);<br/>
float test_moneyWithdraw(float balance);<br/>
void test_menuExit(void);<br/>
void test_errorMessage(void);<br/>



void setUp(){}

void tearDown(){}


int main()
{

  UNITY_BEGIN();


  RUN_TEST(test_login);<br/>
  RUN_TEST(test_checkBalance);<br/>
  RUN_TEST(test_moneyDeposit);<br/>
  RUN_TEST(test_moneyWithdraw);<br/>
  RUN_TEST(test_menuExit);<br/>
  RUN_TEST(test_errorMessage);<br/>

  
  return UNITY_END();
<br/>}

