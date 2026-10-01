# lc29
class Solution:
    def divide(self, dividend: int, divisor: int) -> int:
        if dividend==-2**31 and divisor==-1:
            return 2**31-1
        neg=(dividend<0)!=(divisor<0)
        dividend=abs(dividend)
        divisor=abs(divisor)
        ans=0
        while dividend>=divisor:
            temp=divisor
            count=1

            while dividend>=temp+temp:
                temp+=temp
                count+=count
            dividend-=temp
            ans+=count
        if neg:
            return -ans
        return ans

        
