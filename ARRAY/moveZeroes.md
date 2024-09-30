#### 283. Move Zeroes

```C++
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
    int j = -1;
    for (int i=0; i<nums.length() ; i++) {
        if (nums[i] == 0) {
            j = i;
            break;
        }
    }
    if (j == -1) return a;
    for (int i = j + 1; i < n; i++) {
        if (nums[i] != 0) {
            swap(nums[i], nums[j]);
            j++;
        }
    }
    return nums;
    }
};
```
