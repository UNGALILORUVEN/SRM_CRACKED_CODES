**1). GATE Aspirants**

    #include<stdio.h>
    #include<stdlib.h>
    int main() {
    	//code
    	int t,i,j,n,pos,max;
    	scanf("%d",&t);
    	for(i=0;i<t;i++)
    	{
    	    scanf("%d",&n);
    	    int *arr=malloc(sizeof(int)*n);
    	    for(j=0;j<n;j++)
    	    scanf("%d",&arr[j]);
    	    max=arr[0];
    	    pos=0;
    	    for(j=1;j<n;j++)
    	    {
    	        if(max<arr[j])
    	        {max=arr[j];
    	            pos=j;
    	        }
    	    }
          
     	 	if(pos == n-1)
      	    printf("Ascending with maximum element %d\n", max);
     	 	else if(pos == 0)
      		  {
       		   if((arr[pos] > arr[pos+1]) && (arr[pos+1] < arr[pos+2]))
       	 	    printf("Ascending rotated with maximum element %d\n", max);
       	 	  else
       		     printf("Descending with maximum element %d\n", max);
      		  }
     		else {
     		  if(arr[pos] > arr[pos-1])
       			 printf("Descending rotated with maximum element %d\n", max);
      			}
       	 }
    	return 0;
    }

**2). Thorow this Dupes**

    #include <stdio.h>
    int main()
    {
      int a[20],i,j,k,n;
      scanf("%d",&n);
      for(i=0;i<n;i++)
      {
        scanf("%d",&a[i]);
      }
      for(i=0;i<n;i++)
      {
        for(j=i+1;j<n;)
        {
          if(a[j]==a[i])
          {
            for(k=j;k<n;k++)
            {
              a[k]=a[k+1];
            }
            n--;
          }
          else
          {
            j++;
          }
        }
      }
      for(i=0;i<n;i++)
      {
        printf("%d ",a[i]);
      }
     return 0;
    }
**3). Giant Element**

    #include <stdio.h>
    int main()
    {
      int a[100],i,j,n,t;
      scanf("%d",&n);
      for(i=0;i<n;i++)
      {
        scanf("%d",&a[i]);
      }
      for(i=0;i<n;i++)
      {
        for(j=i+1;j<n;j++)
        {
          if(a[i]>a[j])
          {
            t=a[i];
            a[i]=a[j];
            a[j]=t;
          }
        }
      }
      printf("Sticker with value %d is the biggest",a[i-1]);
     return 0;
    }
**4). Rakshan and his Corns**

    #include <stdio.h>
    int main()
    {
      int a[50],i,n,l,s;
      scanf("%d",&n);
      for(i=0;i<n;i++)
        scanf("%d",&a[i]);
      l=s=a[0];
      for(i=1;i<n;++i)
      {
        if(a[i]>l)
           l=a[i];
        if(a[i]<s)
           s=a[i];
      }
           printf("%d",l);
           printf("\n%d",s);
     return 0;
    }
**5). Catch the Second**

    #include <stdio.h>
    int main()
    {
      int a[50],size,i,j=0,big,sbig;
      scanf("%d",&size);
      for(i=0;i<size;i++)
        scanf("%d",&a[i]);
      big=a[0];
      for(i=1;i<size;i++)
      {
        if(big<a[i])
        {
          big=a[i];
          j=i;
        }
      }
      sbig=a[size-j-1];
      for(i=1;i<size;i++)
      {
        if(sbig<a[i]&&j!=i)
          sbig=a[i];
      }
      printf("%d",sbig);
     return 0;
    }
**6). Memory and Crow**

    #include <stdio.h>
    #include <stdlib.h>
    int main(int argc, char *argv[]) {
    	int n;
    	scanf("%d",&n);
    	int i;
    	int a[100000];
    	for(i=0;i<n;i++){
    		scanf("%d",&a[i]);
    	}
    	for(i=0;i<n-1;i++){
    		printf("%d ",a[i]+a[i+1]);
    	}
    	printf("%d\n",a[i]);
    	return 0;
    }
**7). Corporate Instructor**

    /* C Program to Count Even and Odd Numbers in an Array */
    #include<stdio.h>
     
    int main()
    {
     int Size, i, j = 0, a[10];
     int Even_Count = 0, Odd_Count = 0;
    scanf("%d", &Size);
     for(i = 0; i < Size; i++)
     {
       scanf("%d", &a[i]);
     }
      
     while(j < Size)
     {
        if(a[j] % 2 == 0)
        {
     	Even_Count++;
        }
        else
        {
     	Odd_Count++;
        }
        j++;
     }
     printf("\n%d", Even_Count);
     printf("\n%d", Odd_Count);
     return 0;
    }
**48). Stones**

    #include <stdio.h>
    int main()
    {
      int a,i,j,temp;
      scanf("%d",&a);
      int arr[a];
      for(i=0;i<a;i++)
        scanf("%d",&arr[i]);
      for(i=0;i<a;i++)
      {
        for(j=i;j<a;j++)
        {
          if(arr[i]>arr[j])
          {
            temp=arr[i];
            arr[i]=arr[j];
            arr[j]=temp;
          }
        }
      }
      for(i=0;i<a;i++)
        printf("%d ",arr[i]);
    
     return 0;
    }
**9). Arulmozhivarman The Researcher**

    #include <stdio.h>
    #include <stdlib.h>
    #include <string.h>
    
    /*
     * 
     */
    int main(int argc, char** argv) {
        int t,i;
        char id[1000];
        int alp[27];
        
        scanf("%d", &t);
        while (t-- > 0) {
            memset(id,0,sizeof(id));
            memset(alp,0,27 * sizeof(int));
            scanf("%s",id);
            int n = strlen(id);
            for (i = 0; i < n / 2; i++) {
                alp[id[i] - 'a']++;
            }
            int dev = ((n & 1) != 0 ? 1 : 0);
            for (i = n / 2 + dev; i < n; i++) {
                alp[id[i] - 'a']--;
            }
            
            for (i = 0; i < 27; i++) {
                if (alp[i] != 0) {
                    printf("NO\n");
                    break;
                }
            }
            if (i == 27) 
            {
                printf("YES\n");
            }
        }
        return 0;
    }
**10). Prithiv Shaw and His Friends**

    #include <stdio.h>
    #define MAX_SIZE 100
    
    int main()
    {
        int arr[MAX_SIZE];
        int i, n, sum=0;
    
        /* Input size of the array */
        scanf("%d", &n);
    
        /* Input elements in array */
        for(i=0; i<n; i++)
        {
            scanf("%d", &arr[i]);
    
            // Add each array element to sum
            sum += arr[i];
        }
    
        printf("%d", sum);
    
        return 0;
    }

**11). Dog and the Coins**

        #include <stdio.h>
        int main()
        {
            int t,n,k;
            scanf("%d",&t);
            int i=0,j=0,max=0;
            for(i=0;i<t;i++)
            {
            scanf("%d%d",&n,&k);
            for(j=1;j<=k;j++)
            {
                if((n%j)>max)
                {
                    max=n%j;
                }
            }
           printf("%d\n",max);
           max=0;
        }
        return 0;
      }


