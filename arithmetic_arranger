def arithmetic_arranger(problems,answer = False):
  arranged_problems = []
  #too many problems.
  if len(problems) > 5 :
    return("Error: Too many problems.")

  #operator must be "+" or "-".
  for problem in problems :
    
    operand1,operator,operand2 = problem.split()
    
    if operator not in "-+" :
      return("Error: Operator must be '+' or '-'.")
    
    #operands must only be digits.  
    if operand1.isdigit() is True and operand2.isdigit() is True :
      None
    else :
      return("Error: Numbers must only contain digits.")

    #too many digits.
    result1 = len(operand1) <= 4
    result2 = len(operand2) <= 4
    
    if result1 is True and result2 is True :
      None
    else :
      return("Error: Numbers cannot be more than four digits.")

    width = max(len(operand1),len(operand2)) + 2
    
    #formating each line.
    line1 = f"{operand1.rjust(width)}"
    line2 = f"{operator}{operand2.rjust(width-1)}"
    line3 = "-" * width

    #arranging the problems.
    if answer is False :
      try:
        arranged_problems[0] += (" " * 4)+ line1
      except IndexError:
        arranged_problems.append(line1)
      try:
        arranged_problems[1] += (" " * 4)+ line2
      except IndexError :
        arranged_problems.append(line2)
      try:
        arranged_problems[2] += (" " * 4)+ line3
      except IndexError :
        arranged_problems.append(line3)
      #return(f"{arranged_problems[0]}\n{arranged_problems[1]}\n{arranged_problems[2]}")
    elif answer is True :
      if operator == "+" :
        solution = int(operand1) + int(operand2)
        solution = str(solution)
      else :
        solution = int(operand1) - int(operand2)
        solution = str(solution)
      line4 = f"{solution.rjust(width)}"
      try:
        arranged_problems[0] += (" " * 4)+ line1
      except IndexError:
        arranged_problems.append(line1)
      try:
        arranged_problems[1] += (" " * 4)+ line2
      except IndexError :
        arranged_problems.append(line2)
      try:
        arranged_problems[2] += (" " * 4)+ line3
      except IndexError :
        arranged_problems.append(line3)
      try:
        arranged_problems[3] += " " * 4 + line4
      except IndexError :
          arranged_problems.append(line4)
      #print(arranged_problems)
      #return(f"{arranged_problems[0]}\n{arranged_problems[1]}\n{arranged_problems[2]}\n{arranged_problems[3]}")
  if answer is False :
    return(f"{arranged_problems[0]}\n{arranged_problems[1]}\n{arranged_problems[2]}")
  else :
    return(f"{arranged_problems[0]}\n{arranged_problems[1]}\n{arranged_problems[2]}\n{arranged_problems[3]}")
#print(arithmetic_arranger(["32 + 8","1 - 3801","9999 + 9999","523 - 49"]))

