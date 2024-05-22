# 18.05.2024-Individual-Task-Python

welcome_string = "Good day in Bank Europe!" 
print(welcome_string)

deposit_amounts = [] 
total_balance = 0
try:
  deposit_balance = float(input('Please enter amount of money you want to deposit: '))

  if deposit_balance > 0:
    deposit_amounts.append(deposit_balance)
    total_balance += deposit_balance
    print('Deposit amount is added to your total balance') 
  else:
   print('Deposit amount is not valid. Please try again!')

except Exception as e:
  print(f'wrong input, please enter a numbers: {e}')

while True:
  deposit_balance = input('Would you like to add more deposit to your balance? If not please write"Stop"')
  if deposit_balance == 'Stop':
    print('You have written "Stop". You finished add deposit!') 
    print('See you next time!') 
    break
else:
    try:
       deposit_balance = float(deposit_balance)
       if deposit_balance > 0:
          deposit_amounts.append(deposit_balance)
          total_balance += deposit_balance
          print('Deposit amount is added to your total balance') 
       else:
          print('Deposit amount is not valid. Please try again!')

    except Exception as e:
      print(f'wrong input, please enter a numbers: {e}')

print(f'Your total balance is: {deposit_amounts}')  

try:
    withdraw_amount = float(input('Please enter amount of money you want to withdraw: '))
    if withdraw_amount > 0 and withdraw_amount <= total_balance:
      total_balance -= withdraw_amount
      print('Withdrawal successful')
    else:
      print('Withdrawal amount is not valid. Please try again!')
 except Exception as e:
      print(f'wrong input, please enter a numbers: {e}')



  
