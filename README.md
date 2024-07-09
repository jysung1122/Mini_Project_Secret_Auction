# Mini_Project_Secret_Auction
2024.07.09 ~ 2024.07.09
### 비밀 경매 프로그램이란?
- 한 대의 노트북으로 여러명의 유저가 번갈아 가며 이름과 입찰할 가격을 입력하면 가장 높은 금액을 입력한 정보를 출력함

### Flow Chart
<img width="669" alt="image" src="https://github.com/jysung1122/aiModel/assets/56614779/7d8d1aac-4cb1-4c34-a9c8-728a658b386a">

### 코딩
```
import art
from replit import clear

print(art.logo)
print("Welcome to the secret auction program.")

name_and_bid = {}
winner_name = ""
winner_bid = 0

end_of_program = False
while not end_of_program:
    name = input("What is your name?: ")
    bid = int(input("What's your bid?: "))

    name_and_bid[name] = bid

    continue_game = input("Are there any other bidders? Type 'yes' or 'no.'\n").lower()
    if continue_game == "yes":
        clear()
    elif continue_game == "no":
        end_of_program = True

for key in name_and_bid:
    if name_and_bid[key] > winner_bid:
        winner_name = key
        winner_bid = name_and_bid[key]

print(f"The winner is {winner_name} with a bid of ${winner_bid}.")
        
```
