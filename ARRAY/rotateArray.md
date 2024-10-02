### 189. Rotate Array

```C++
  class Solution {
public:
    void rotate(vector<int>& nums, int k) {
        int n = nums.size();
        k = k % n;
        reverse(nums.begin(), nums.end());  //reverse: array
        reverse(nums.begin(), nums.begin() + k); //reverse: first k ele
        reverse(nums.begin() + k, nums.end()); //reverse: after k ele
    }
};
```
