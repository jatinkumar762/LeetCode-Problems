### My Solution

```
class Solution
{
    public int strStr(String haystack, String needle) 
    {
        if(needle.length()==0)
            return 0;
        
        if(haystack.length()==0)
            return -1;       
        
        for(int i=0;i<haystack.length();i++)
        {
            int j=0;
            int k=i;
            while(j<needle.length()&&k<haystack.length()&&needle.charAt(j)==haystack.charAt(k))
            {
                j++;
                k++;
            }
            if(j==needle.length())
                return i;
        }
        return -1;
        
    }
}
```
