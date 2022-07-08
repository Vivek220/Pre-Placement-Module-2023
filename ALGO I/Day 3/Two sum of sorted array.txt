class Solution {
    public int[] twoSum(int[] numbers, int target) {
        int i=0;int j=numbers.length-1;
        int mid;
        int res[]=new int[2];
        while(i<=j){
            mid=numbers[i]+numbers[j];
            if(mid==target){
                res[0]=i+1;
                res[1]=j+1;
                return res;
            }else if(mid>target){
                j--;
            }else{
                i++;
            }
        }
        return res;
       
    }
}