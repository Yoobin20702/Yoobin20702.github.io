---
layout: single
title: "조건문"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: 형성평가
---

###01.사주보기
![saju](/assets/images/if1.jpg)
~~~c
#include<stdio.h>
 int main(void)
 {  int year,month,day,result;
  
    printf("당신의 사주를 봐드립니다.\n");
    printf("연도 월 일을 차례로 입력하세요 : ");
    scanf("%d,%d,%d,&year,&month,&day);
          
    result=(year-month+day)%10;
    if(result==0)
     printf("당신의 사주는 대박입니다.\n");
  else
     printf("당신의 사주는 그럭저럭입니다.\n");
    return 0;
 }
~~~


###02.3개의 터널 통과
![tunnel](/assets/images/if2.jpg)
~~~c
#include <stdio.h>
 int main(void)
 {  int tunnel_1, tunnel_2, tunnel_3;
  printf("세 터널의 높이를 차례대로 입력하세요 : ");
  scanf("%d,%d,%d,&tunnel_1,&tunnel_2,&tunnel_3);
  if(tunnel_1<=170)
    printf("충돌 %d", tunnel_1);
  else if(tunnel_2<=170)
    printf("충돌 %d", tunnel_2);
  else if(tunnel_3<=170)
    printf("충돌 %d", tunnel_3);
  else
    printf("무사 통과");
  return 0;
        }
 ~~~
 
 
 ###03.이 달은 며칠까지 있을까?
 ![callender](/assets/images/if3.jpg)
 ~~~c
#include <stdio.h>
 int main(void)
 {  int year, month;
  
    printf("연도와 월을 입력하세요 : ");
    scanf("%d%d", &year, &month);
    printf("%d년 %d월의 마지막날은 ", year, month);
  
    if(month==1||month=3||month==5||month==7||month==8||month==10||month==12)
      printf("31일");
    else if(month==4||month==6||month==9||month==11)
      printf("30일");
    else 
    {
       if((year%4==0 && year%100!=0) || year%400==0)
      printf("29일");
    else
      printf("28일");
    }
    printf("입니다.\n")
    return 0;
 }
~~~
