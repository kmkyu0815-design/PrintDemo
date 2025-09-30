# main_print_v1.py
# 파이썬의 print() 기본 활용법 예제

# 1. 기본 출력
print("안녕하세요, Python!")

# 2. 여러 값 출력 (sep 기본값은 공백)
print("Hello", "World", 2025)

# 3. sep 옵션 사용
print("apple", "banana", "cherry", sep=", ")

# 4. end 옵션 사용 (줄바꿈 대신 다른 문자)
print("첫 번째 줄", end=" -> ")
print("두 번째 줄")

# 5. 줄바꿈(\n), 탭(\t) 포함
print("한 줄\n두 줄\n세 줄")
print("이름\t나이\t직업")

# 6. f-string
name = "민규"
age = 25
print(f"제 이름은 {name}이고, 나이는 {age}살입니다.")

# 7. str.format()
print("오늘은 {}년 {}월 {}일".format(2025, 9, 23))

# 8. 숫자 포맷팅
pi = 3.1415926535
print("원주율: {:.2f}".format(pi))
print(f"원주율: {pi:.4f}")

# 9. 정렬
print("{:<10}".format("왼쪽"))
print("{:>10}".format("오른쪽"))
print("{:^10}".format("가운데"))

# 10. 이스케이프
print("따옴표 출력: \"Hello\"")
print("역슬래시 출력: \\")

# 11. 여러 줄 문자열
print("""
여러 줄을
그대로 출력합니다.
""")


# main_print_v2.py
# rich 라이브러리를 활용한 print 예제
# 설치 필요: pip install rich

from rich import print
from rich.panel import Panel
from rich.table import Table

# 1. 색상/스타일 있는 텍스트
print("[bold magenta]Hello, Python![/bold magenta]")
print("[green]성공적으로 실행되었습니다![/green]")

# 2. Panel 출력
print(Panel("이건 [cyan]Panel[/cyan] 안에 들어간 텍스트입니다.", title="패널 예제"))

# 3. Table 출력
table = Table(title="회원 목록")
table.add_column("이름", justify="center", style="cyan")
table.add_column("나이", justify="right", style="magenta")
table.add_column("직업", justify="center", style="green")

table.add_row("민수", "20", "학생")
table.add_row("지영", "30", "개발자")
table.add_row("현우", "28", "디자이너")

print(table)

# 4. sep / end 옵션도 그대로 사용 가능
print("[yellow]하나[/yellow]", "[yellow]둘[/yellow]", "[yellow]셋[/yellow]", sep=" | ")
print("[red]끝![/red]", end=" ***\n")
