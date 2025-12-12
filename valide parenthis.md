# You are given a string s consisting only of the characters 'L' and 'R'. A substring is balanced if it contains an equal number of 'L' and 'R'. # Return the maximum number of balanced substrings you can obtain by splitting the string.

# Constraints: # 1 ≤ len(s) ≤ 10^5 # s contains only 'L' and 'R' # Example: # Input: s = "RLRRLLRLRL" # Output: 4

s = ["RLRRLLRLRL"]   # <-- This makes s a LIST containing one string



def cycleCount():
  count=0
  balance=0
  


s = "RLRRLLRLRL"

def balancedStringsplit(s):
    count = 0
    balance = 0

    for c in s:
        if c == 'R':
            balance += 1
        else:
            balance -= 1

        if balance == 0:
            count += 1

    return count

balancedStringsplit(s)


✅ Output:
4



>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
def count_valid_parentheses(exp):
    balance = 0
    groups = 0

    for ch in exp:
        if ch == '(':
            balance += 1
        else:
            balance -= 1

        if balance == 0:
            groups += 1

    return groups


expr = "(()())()(()())"

print("Input:", expr)
print("Valid parentheses groups:", count_valid_parentheses(expr))
