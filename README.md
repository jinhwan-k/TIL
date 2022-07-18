# TIL
class Solution {
    public String solution(String s1) {      //s1 이라는 문자에 대해
        String answer = "";               //""answer에 아무것도 없음.공백을 대입
        int cnt = 0;                     //  변수생성      
        String[] strArr = s1.split("");// 문자열 → 문자열배열 , s1을 ""으로 나눔
                                       //문자열배열에 나눈 s1 대입

        for(String s2 : strArr){    //나눈 s1을 s2(두번째)에 대입. 반복
        if(s2.contains(" ")){       //contains는 특정문자열이 들어있는지 확인하느 함수. 즉 ""가 s2에 들어있다면,
                cnt=0;          //cnt변수는 0이다.
        }
            else                //아니라면
            cnt++;              //cnt는 숫자가 올라간다
            if(cnt%2 == 0){     //만약 cnt를 나눈값의 나머지가 0이라면,짝수
            answer += s2.toLowerCase();   //s2는 소문자 
            } else {                      //s2는 대문자 
            answer += s2.toUpperCase();
              }
        }
            return answer;                 
    }
}
