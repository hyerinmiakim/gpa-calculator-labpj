# 학점계산기
### 임베디드SW공학 프로젝트

#### * **개요**
본 프로젝트는 매 학기 취득학점 기준의 잦은 변동으로 혼란을 겪을 학생들을 위해 제작하였다. 프로젝트의 확실한 수요와 필요성을 위해 학과학생들을 대상으로 
설문조사를 실시하였다. 학점관리에 어려움을 겪고 있다는 문항에 동의를 표한 학생들은 저학년일 것이다라는 예측과 달리 다양한 학년군의 학생들에게 
'그렇다'라는 답변을 얻을 수 있었다. 이 결과로 인해 우리는 학생들이 사용하기 쉽고 간단한 기능을 만들어야 겠다는 목표를 설정할 수 있었다.  

#### * **SW 파일 구성**

**1.funnel_a2.c**
•	과목들의 정보가 담긴 파일 2018_ese.xlsx파일을 데이터로 읽기 위해 csv파일로 변환해준다.
•	각 이수구분별로 고유의 알파벳 식별자를 달아준다 (교양필수: a, 전공기초: b, 전공선택: c, 전공필수: d).
•	이차원 배열에 **이수구분별로** 데이터를 저장하고 리턴한다.

**2.	printinfo.c**
-	유저가 입력한 과목에 대한 정보를 알려준다.
-	사용자가 정보를 얻고자 하는 과목명을 입력 받고, funnel_a2.c에서 리턴한 배열(데이터가 들어있는 배열)을 인자로 받아, 배열에서 해당 과목을 검색한다.
-	이차원 배열에 해당 과목의 이수구분, 학년, 코드, 과목명, 교수명, 학점 등 **사용자가 원하는 정보**를 저장하고 리턴한다.
-	이 배열을 리턴함으로써 다른 함수에서 정보들의 이용이 쉽다.

**3.	gpa.c**
-	사용자에게 이름과 학번을 입력 받는다. 그리고 사용자는 자신이 이수한 과목명과 성적을 모두 입력해 파일에 저장한다. 기입한 점수를 학점대로 계산하는데, 총 학점, 전공학점 대로 나눠서 출력한다.

**4.	graduate.c**
-	해당 학생이 현재까지 이수한 교양, 전공 등에 대한 정보를 알려준다. 예를 들어, “교양 30학점, 전공 70학점을 이수했기 때문에 졸업을 위해서는 전공 2학점 이상이 요구됩니다” 라고 알려준다.

**5.	printGrades.c**
-	사용자의 학번을 입력 받은 뒤, 그 사용자가 그동안 이수했던 과목들에 대한 학점 정보를 알려준다. 
 
