from art import logo
import random
from replit import clear

should_continue = True
answer = input("Do you want to play a game of Blackjack? Type 'y' or 'n': ")
if(answer == 'y'):
  should_continue = True
else:
  should_continue = False
while should_continue:
  print(logo)
  user_list = []
  computer_list = []
  cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
  user_list.extend([cards[random.choice(cards)],cards[random.choice(cards)]])
  computer_list.extend([cards[random.choice(cards)],cards[random.choice(cards)]])
  

  def calculate(list):
      # sum = 0
      # for i in range(0,len(list)):
      #   sum += list[i]
      # return sum
    return sum(list)
  print(f"Your cards: {user_list}, current score: {calculate(user_list)}")
  print(f"Computer's first card: {computer_list[0]}")
  
  def result(user_list, computer_list):
      print(f"Your final hand: {user_list}, final score: {calculate(user_list)}")
      print(f"Computer's final hand: {computer_list}, final score: {calculate(computer_list)}")
      if(calculate(user_list) == 21):
        print("You win with Blackjack.")
      elif (calculate(computer_list) == 21):
        print("You lose. Computer wins with Blackjack.")
      elif(calculate(user_list) > 21 and calculate(computer_list) < 21):
        print("You lose.")
      elif(calculate(computer_list) >21 and calculate(user_list) < 21):
        print("You win.")
      elif(calculate(user_list) < calculate(computer_list)):
        print("You lose.")
      elif(calculate(user_list) > calculate(computer_list)):
        print("You win.")
      elif(calculate(user_list) == calculate(computer_list)):
        print("Draw")
        
  def another (user_list, computer_list):
    another = input("Type 'y' to get another card, type 'n' to pass: ")
    if another == 'y':
      user_list.append(cards[random.choice(cards)])
      print(f"Your cards: {user_list}, current score: {calculate(user_list)}")
      print(f"Computer's first card: {computer_list[0]}")
      blackjack(user_list, computer_list)
    else:
      computer_list.append(cards[random.choice(cards)])
      while(calculate(computer_list) < 17):
        computer_list.append(cards[random.choice(cards)])
      if calculate(computer_list) > 21:
        result(user_list, computer_list)
      else:
        result(user_list, computer_list)
  def blackjack(user_list, computer_list):
    if calculate(user_list) == 21 or calculate(computer_list)==21:
      result(user_list,computer_list)
    else:
      if calculate(user_list) > 21:
        for j in range(0, len(user_list)):
          if user_list[j] == 11:
            user_list[j] = 1
        if(calculate(user_list) > 21):
          result(user_list, computer_list)
        else:
          another(user_list, computer_list)       
      else:
        another(user_list, computer_list)            
  blackjack(user_list, computer_list)   
  answer = input("Do you want to play a game of Blackjack? Type 'y' or 'n': ")
  if(answer == 'y'):
    should_continue = True
    clear()
  else:
    should_continue = False 
