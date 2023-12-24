# minimum-changes-to-make-alternating-binary-string

class Solution:
    def minOperations(self, s):
        operations = 0

        for i in range(len(s)):
            expected = '0' if i % 2 == 0 else '1'
            operations += (s[i] != expected)

        return min(operations, len(s) - operations)


s1 = "0100"
obj = Solution()
print(obj.minOperations(s1))  

s2 = "10"
print(obj.minOperations(s2))  

s3 = "1111"
print(obj.minOperations(s3))  

s4 = "110010"
print(obj.minOperations(s4))  
