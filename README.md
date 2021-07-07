# step-sourcecode
***
#include <stdio.h>

int main(void) {
	/*
		입력 받을 데이터 개수를 의미하는 n 변수,
		시작지점과 끝지점을 의미하는 start, end 변수,
		거리를 의미하는 distance 변수,
		최소 스텝수를 계산하기 위한 d 변수,
		최소 스텝수를 의미하는 step 변수를 각각 int형으로 선언.
	*/
	int n, start, end, distance, step, d;
	scanf("%d", &n); // 몇 개의 시작지점과 끝지점을 입력받을지 결정. 
	for( ; n>0; n--) { // 입력받은 변수 n의 개수만큼 for문 실행. 
		scanf("%d %d", &start, &end); // 시작지점과 끝지점 입력받음. 
		distance = end - start; // 끝지점에서 시작지점을 뺄셈하여 두 지점 사이의 거리를 구함.
		
		/*
			최소 스텝수를 구해야하므로 최소 스텝수를 의미하는 step의 값을 1씩 증가시키고, 
			그때마다 변수 d와 step의 합이 거리를 의미하는 변수 distance보다 작을 경우에만 동작하는 for문 실행. 
		*/
		for(step=d=0; (d+step)<distance; step++) 
			/*
				따로 첨부한 풀이과정과 같이 변수 d에는 step/2가 계속 더하기 되는 것을 알 수 있으므로
				step의 값이 1씩 증가할 때마다 d에 step/2의 값을 계속 더하면서 저장. 
			*/
			d += step/2;
						
		printf("Result : %d \n", step); // 최소 스텝수인 변수 step을 출력. 
	}
	return 0;
}
