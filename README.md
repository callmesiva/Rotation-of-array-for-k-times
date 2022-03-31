# Rotation-of-array-for-k-times

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
