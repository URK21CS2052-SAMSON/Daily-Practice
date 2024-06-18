#palindrome  check



import re
class Solution:
    def isPalindrome(self, s: str) -> bool:
        
        a = re.findall(r'[a-zA-Z0-9]',s)
        result = ''.join(a).lower()
        # b = result
        # c = b.lower()
        
        stack = list(result)
        reversed_string = ''
        while stack:
            reversed_string += stack.pop()
        
        if reversed_string == result:
            return True
        else:
            return False
        
