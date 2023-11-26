# Decompress-Run-Length-using-Java-Leetcode
      
      class Solution {
          public int[] decompressRLElist(int[] nums) {
              int arrSize =0;
              for(int i =0; i<nums.length;i=i+2){
                  arrSize += nums[i];
              }
              int[] arr = new int[arrSize];
              int k = 0;
              int freq = 0;
              int val = 1;
              while(freq <= nums.length && val <= nums.length){
                  for(int i =0;i<nums[freq];i++){
                      arr[k] = nums[val];
                      k++;
                  }
                  freq = freq + 2;
                  val = val + 2;
              }
              return arr;
          }
      }
