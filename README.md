# Studying-Python
learning python
파이썬 기초 연습

import sys
def py2_or_py3():
    
    major = sys.version_info.major
    print("======>", major)

    if major < 3:
            return 'Python 2'
    
    else:
            return 'Python 3'

# if 사용해서 성적입력 받고 등급 추출하기

kor = int(input("국어: "))
mat = int(input("수학: "))
eng = int(input("영어: "))

avg = (kor + mat + eng) / 3

print(f"평균: {avg:.2f}")

if avg >= 90:
    print("등급: A")

elif avg >= 80:
    print("등급: B")

elif avg >= 70:
    print("등급: C")

elif avg >= 60:
    print("등급: D")

else:
    print("등급: F")

# version 2

score = int(input("점수: "))

if score >= 90:
    print("등급: A")

elif score >= 80:
    print("등급: B")

elif score >= 70:
    print("등급: C")

elif score >= 60:
    print("등급: D")

else:
    print("등급: F")

# for 이용하여 구구단 만들기

def 구구단():

    for i in range(0,8):
        
        print(f"{i + 2}단".center( 10, "="))
        
        for j in range(0,9):
            
            # print(f"{i+2} 곱하기 {j+1}은")
            # print(f"{i+2} * {j+1} = {(i+2) * (j+1)}")
            print("%d * %d = %2d" %(i+2, j+1, (i+2) * (j+1)))

구구단()


# version 2

def 구구단2():
    앞수들 = [2, 3, 4, 5, 6, 7, 8, 9]
    뒷수들 = [2, 3, 4, 5, 6, 7, 8, 9]
    for 앞수 in 앞수들:
        for 뒷수 in 뒷수들:
            print(f"{앞수}*{뒷수}={앞수 * 뒷수}")

구구단2()

# range 연습

def test():

    m = 50

숫자들 = [1,2,3,4,5]

for 숫자 in 숫자들:
    m = 숫자

print(m)

for i in range(0,10):
    for ii in range(0,10):
        print(i)

# 반복문 활용하기
import pandas as pd
# openpyxl


df = pd.read_excel(r"C:\Users\user\Downloads\우리반친구들.xlsx", sheet_name='Sheet1')

df.columns = ["컬럼1", "컬럼2", "컬럼3"]
이름들 = df["컬럼2"].to_list()

def 반복문기본활용():
    빈리스트 = []

    for i in range(0, len(이름들)):
        빈리스트.append(이름들[i] + " 화이팅!")

    for 이름 in 빈리스트:
        print(이름)

# version2

def 반복문기본활용():
    이름들 = ["가명주",
           "갈기현",
           "강승민",
           "고성균",
           "김남일",
           "김선빈",
           "김선희",
           "김성현",
           "김예진",
           "김윤지",
           "김재윤",
           "김해송",
           "남광영",
           "민찬영",
           "송유진",
           "엄요한",
           "오정현",
           "윤솔미",
           "이승현",
           "장훈희",
           "장희준",
           "조기영",
           "최서린",
           "최치송",
           "홍세나", ]
    빈리스트 = []

    for i in range(0, len(이름들)):
        빈리스트.append(이름들[i] + " 화이팅♥")

    for 이름 in 빈리스트:
        print(이름)

반복문기본활용()

# version 3

def 반복문기본활용():
    신상정보 = []
    이름들 = ["홍길동", "이순신", "세종대왕"]
    나이들 = [20, 30, 40]
    직업들 = ["학생", "선생님", "교장선생님"]
    # 포문으로 자료구조에 값넣기
    for i in range(0,len(이름들)):
        신상정보.append({"이름": 이름들 [i], "나이": 나이들[i], "직업": 직업들[i]})
        #print(신상정보[2]["나이"])
    print(f"세종대왕의나이는 {신상정보[2]['나이'] }야 ")


    for i in range(0,len(신상정보)):
        item = 신상정보 [i]
        항목들 = list(item.keys())
        값들 = list(item.values())


        for j in range(0, len(항목들)):
            print (f"{항목들[j]}는, {값들[j]}입니다")

    for i in range(0, len(신상정보)):
        print(f"이름은 {신상정보[i]['이름']}, 나이는{신상정보[i]['나이']} 직업은{신상정보[i]['직업']}입니다 ")

반복문기본활용()

# version 4

def 반복문기본활용():

    이름들 = ["홍길동", "이순신", "세종대왕"]

    빈리스트 = []
    # list(map(빈리스트))
    #
    for i in range(0, len(이름들)):
         빈리스트.append(이름들[i] + " 화이팅♥")
    # 정의부
    # def 인사하는함수(이름):
    #     return 이름 + "안녕하세요"

    결과리스트 = list(map(lambda x : x+"안녕하세요", 빈리스트))
    print(빈리스트)

반복문기본활용()

# version 5

def 반복문기본활용():
    빈딕 = {}

    #포문으로 자료구조에 값넣기
    for i in range(0,10):
        빈딕["이름"] = "홍길동"
        빈딕["나이"] = 20
        빈딕["직업"] = "학생"

    print(빈딕)

반복문기본활용()

# while 연습

def 와일문연습():

    합계 = 0
        #조건
    while 1==1:
        합계 += 1
        if 합계 == 100:
            break

    print(합계)

와일문연습()

# 스트링 연습

def 스트링연습():
    신상정보 = ["홍길동", 20, "학생" ]
    신상정보2 = {"이름":"홍길동", "나이":20, "직업":"학생"}
    print("이름은 {0} 나이는 {1} 직업은 {2}".format(*신상정보))
    print("이름은 {이름} 나이는 {나이} 직업은 {직업}".format(**신상정보2))

스트링연습()









            

