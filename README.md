# To-find-numbers-that-disappeared-in-an-Array
class Solution {
    public List<Integer> findDisappearedNumbers(int[] nums) {
    for (int i = 0; i < nums.length; i++) {
        int index = Math.abs(nums[i]) - 1; //as array index start from 0 and in question its starting from 1 so to initialise index from zero we subtract 1 from every number of the array
        nums[index] = Math.abs(nums[index]) * -1; //for marking the values
    }
    
    List<Integer> res = new ArrayList<>();
    
    for (int i = 0; i < nums.length; i++) {
        if (nums[i] > 0) {
            res.add(i + 1);
        }
    }
    
    return res;
}
    }
