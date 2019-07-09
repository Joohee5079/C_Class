# C_Class
190709(1)


#include <stdio.h>

void main()
{
	const int su = 3;
	int Ko, Eg, Ma, t; // Ko=Korean, Eg=English, Ma=Math, t=total
	float a;
	char n[10], g; // g = grade(점수)

	printf("이름을 입력하세요 : ");
	scanf_s("%s", n, sizeof(n));
	//sizeof(n) 메모리 용량 절약을 위한?
	//예외 처리 루틴 : 예외 상황에 대비하여 처리하고 정상적인 작업을 계속하거나 작업을 끝마치도록 하는 일

	printf("국어 점수를 입력하세요 : ");
	scanf_s("%d", &Ko);

	printf("영어 점수를 입력하세요 : ");
	scanf_s("%d", &Eg);

	printf("수학 점수를 입력하세요 : ");
	scanf_s("%d", &Ma);


	t = Ko + Eg + Ma;
	a = t / su; //a = average(평균)

	if (a >= 90) g = 'A';
	else if (a >= 80) g = 'B';
	else if (a >= 70) g = 'C';
	else if (a >= 60) g = 'D';
	else g = 'F';

	printf("\n--- 결 과 ---\n");
	printf("이름 : %s \n총점 : %d \n평균 : %.2f \n학점 : %c", n, t, a, g);
	// %.2f 소수점 3번째 자리에서 반올림하여 2번째 자리까지 출력
	printf("\t\t\t수고하셨습니다.");
}
