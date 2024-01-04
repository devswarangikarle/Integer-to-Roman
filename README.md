# Integer-to-Roman

class Solution:
    def intToRoman(self, num):
        result = ""
        roman_mapping = {
            1000: "M",
            900: "CM",
            500: "D",
            400: "CD",
            100: "C",
            90: "XC",
            50: "L",
            40: "XL",
            10: "X",
            9: "IX",
            5: "V",
            4: "IV",
            1: "I"
        }

        for value, symbol in roman_mapping.items():
            while num >= value:
                result += symbol
                num -= value

        return result


solution = Solution()
print(solution.intToRoman(3))   
print(solution.intToRoman(58))  
print(solution.intToRoman(1994)) 
