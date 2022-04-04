# Rotation-of-array-for-k-times-without-new-array

        
        
        int nums[]={1,2,3,4,5};
        int k=4;
        
        boolean counter=true;
        
         if(k == nums.length || nums.length ==1)
         {
           counter=false;
           
           for(int i=0; i<nums.length; i++)
            {
             System.out.println(nums[i]+" ");
             
            }
         }
       
        
    if(counter==true)
     {
        if(k>nums.length)
        {
            k=k%nums.length;
        }
        
        int temp=0;
        int rigth=0;
        int rightend=   ( nums.length - k) -1;
        
        while(rigth < rightend)
        {
            temp=nums[rightend];
            nums[rightend]=nums[rigth];
            nums[rigth]=temp;
            rigth++;
            rightend--;
        }
        
        int left=nums.length-k;
        int leftend= nums.length-1;
        while(left<leftend)
        {
            temp=nums[leftend];
            nums[leftend]=nums[left];
            nums[left]=temp;
            left++;
            leftend--;
        }
        
        int start=0;
        int end=nums.length-1;
        while(start<end)
        {
            temp=nums[end];
            nums[end]=nums[start];
            nums[start]=temp;
            start++;
            end--;
        }

        for(int i=0; i<nums.length; i++)
         {
           System.out.print(nums[i]+" ");
         }
  
     }



# Rotation-of-array-for-k-times-with-new-array

       int arr[]= {1,2,3};
       int rotation =1;
       int rotarr[]= new int [arr.length];
       
       for(int i=0; i<arr.length; i++)
       {
         int temp = (i+rotation)%arr.length;
         rotarr[temp]=arr[i];
       }
       
       for(int i=0; i<arr.length; i++)
       {
         arr[i]=rotarr[i];
       }
        for(int i=0; i<arr.length; i++)
       {
         System.out.print(arr[i]);
       }
