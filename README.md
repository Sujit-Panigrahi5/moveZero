// time complecity :O(n)
// space complecity:O(1)

import java.util.*;
public class MoveZero {
    public static void main(String[] args) {
        int []nums={0,1,0,3,12};
        int p=0;
        int curr=0;
        for(int i=0;i<nums.length;i++){
            if(nums[curr] != 0){
                int temp=nums[p];
                nums[p]=nums[curr];
                nums[curr]=temp;
                curr++;
                p++;
            } else{
                curr++;
            }
        }
        for(int i=0;i<nums.length;i++){
            System.out.print(nums[i]+" ");
        }
        
    } 
}
