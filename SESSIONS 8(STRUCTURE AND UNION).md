**1). Student Data Repository** 
  
    #include<stdio.h>
    struct student
    {
     char name[100];
    struct dateOfBirth
    {
      int rollno,date,month,year;
    }DOB;
    }std;
    int main()
    {
      scanf("%s%d%d%d%d",std.name,&std.DOB.rollno,&std.DOB.date,&std.DOB.month,&std.DOB.year);
      printf("Name=%s\nRollNo=%d\nDate of birth=%d/%d/%d",std.name,std.DOB.rollno,std.DOB.date,std.DOB.month,std.DOB.year);
      return 0;
    }
**2). Phd Fees**

    #include <stdio.h>
    #include<string.h>
    struct student
    {
      int roll;
      char name[100];
      char course[100];
      int fees;
    }s1;  
    int main()
    {
    printf("Details of student");
      scanf("%d",&s1.roll);
      scanf("%s",s1.name);
      scanf("%s",s1.course);
      scanf("%d",&s1.fees);
      printf("\nRoll Number=%d",s1.roll);
      printf("\nName=%s",s1.name);
      printf("\nCourse=%s",s1.course);
      printf("\nFees=%d",s1.fees);
      return 0;
    }
**3). Sonata**

    #include <stdio.h>
    union Time
    {
      int seconds,minutes,hours;
    };
    int main(){
        union Time startTime,stopTime,diff;
        printf("The time difference is\n");
        scanf("%d %d\n",&startTime.hours,&stopTime.hours);
        diff.hours=startTime.hours-stopTime.hours;
        printf("Hours:%d\n",diff.hours);
        scanf("%d %d\n ",&startTime.minutes,&stopTime.minutes);
        diff.hours=startTime.minutes-stopTime.minutes;
        printf("Minutes:%d\n",diff.minutes);
        scanf("%d %d",&startTime.seconds,&stopTime.seconds);
        diff.hours=startTime.seconds-stopTime.seconds;
        printf("Seconds:%d\n",diff.seconds);
        return 0; 
    }
**4). Student Marksheet**

    #include <stdio.h>
    #include<string.h>
    union Student{
      char name[60];
      int tamil,english,maths,science,ss;
    };
    int main() {
      union Student s1;
      printf("Details of student\n");
      scanf("%s",s1.name);
       printf("Name of the student=%s\n",s1.name);
      scanf("%d",&s1.tamil);
      printf("Tamil=%d\n",s1.tamil);
      scanf("%d",&s1.english);
      printf("English=%d\n",s1.english);
      scanf("%d",&s1.maths);
      printf("Maths=%d\n",s1.maths);
      scanf("%d",&s1.science);
      printf("Science=%d\n",s1.science);
      scanf("%d",&s1.ss);
      printf("Social Science=%d",s1.ss);
    	return 0;
    }


**5). Add Up the Distance**

    #include <stdio.h>
    union Distance
    {
      int feet_of_type;
      float inch_of_type;
    };
    int main()
    {
      union Distance d1,d2,sumOfDistances;
      scanf("%d %d\n",&d1.feet_of_type,&d2.feet_of_type );
      sumOfDistances.feet_of_type=d1.feet_of_type+d2.feet_of_type;
      printf("Sum of distances=%d feet\n",sumOfDistances.feet_of_type);
      scanf("%f %f\n",&d1.inch_of_type,&d2.inch_of_type);
      sumOfDistances.inch_of_type=d1.inch_of_type+d2.inch_of_type;    
      printf("Sum of distances=%.2f inches",sumOfDistances.inch_of_type);
      return 0;
    }
**6). History of institution**

        #include <stdio.h>
        #include <string.h>
        struct College 
        {
          char name[100];
          char city[100];
          int establishmentYear;
          float passPercentage;
        };
        int main()
        {
             int lines;
             scanf("%d", &lines);
             struct College S1[lines], temp;
             int count;
             for (count=0; count < lines; count++){
                 scanf("%s", S1[count].name);
                 scanf("%s", S1[count].city);
                scanf("%d", &S1[count].establishmentYear);
                scanf("%f", &S1[count].passPercentage);
        }
        int j;
        for (count = 0; count < lines-1; count++)
        {
            for (j = count+1; j < lines; j++)
            {
                if (strcmp(S1[count].name,S1[j].name) > 0) 
                {
                    temp = S1[count];
                    S1[count] = S1[j];
                    S1[j] = temp;
                }
           }
       }
       printf("Details of colleges\n");
       for (count = 0; count < lines; count++)
       {
          printf("Name:%s\n",S1[count].name);
          printf("City:%s\n",S1[count].city);
          printf("Year of establishment:%d\n",S1[count].establishmentYear);
         printf("Pass percentage:%.1f\n",S1[count].passPercentage);
      }
      return 0;
    }
**7). DISTANCE**

        #include <stdio.h>
        struct Distance
        {
          int feet;
          float inch;
        } 
        d1, d2, sumOfDistances;
        int main()
        {
            scanf("%d %f", &d1.feet, &d1.inch);
            scanf("%d %f", &d2.feet, &d2.inch);
            sumOfDistances.feet = d1.feet + d2.feet;
            sumOfDistances.inch = d1.inch + d2.inch;
            printf("Sum of distances=%d feet and %.2f inches\n",sumOfDistances.feet, sumOfDistances.inch);
            return 0;
        }
 **8). ACCESSING UNION MEMBERS**
 
        #include <stdio.h>
        union Job 
        {
          int workerNo;
        } j;
        int main()
        {
          scanf("%d", &j.workerNo);
          printf("Number of workers = %d\n",j.workerNo);
          return 0;
        }
**9). SRM Admissions**

      #include <stdio.h>
      int main() 
      {
        struct candidate
        {
          char name[80];
          int jeeerank,highersec;
        };
      struct candidate ad;
      scanf("%s",ad.name);
      printf("Name=%s\n",ad.name);
      scanf("%d",&ad.jeeerank);
      printf("JEEE Rank=%d\n",ad.jeeerank);
      scanf("%d",&ad.highersec);
      printf("12th Mark=%d\n",ad.highersec);
		  return 0;
      }
 **10). CGPA**
 
       #include <stdio.h>
       int main() 
       {
          union student
          {
              char name[30];
              char subject[20];
              float percentage;
          };
        union student record;
        scanf("%s",record.name);
        printf("Name: %s\n",record.name);
        scanf("%s",record.subject);
  	    printf("Subject: %s\n",record.subject);
        scanf("%f",&record.percentage);
        printf("Percentage: %.1f",record.percentage);
	      return 0;
      }
  **11). Age**
  
        #include <stdio.h>
        union calci
        {
            int me;
            int you;
        };
        int main() 
        {
          union calci age;
          scanf("%d",&age.me);
  	      printf("I am %d\n",age.me);
          scanf("%d",&age.you);
          printf("You are %d\n",age.you);
	        return 0;
        }
  **12). Play With Number**
  
  	
      include <stdio.h>
      struct fraction
	{
    	int numerator,denominator;
	};
	int main()
	{
    	int div1,div2;
    	struct fraction v1,v2;
    	scanf("%d %d",&v1.numerator,&v1.denominator);
    	scanf("%d %d",&v2.numerator,&v2.denominator);
   	div1=v1.numerator/v1.denominator;
    	div2=v2.numerator/v2.denominator;
    	if(div1>div2) 
      		printf("%d/%d is greater than %d/%d",v1.numerator,v1.denominator,v2.numerator,v2.denominator);
    	else
      		printf("%d/%d is smaller than %d/%d",v1.numerator,v1.denominator,v2.numerator,v2.denominator);

    	return 0;
	}	
**13). Employee**

	#include <stdio.h>
 	struct employee
	{
    	char    name[30];
   	int     empId;
    	float   salary;
	};
 	int main()
	{
 
    		struct employee emp;
     

           	scanf("%s",emp.name);
             	scanf("%d",&emp.empId);
         	scanf("%f",&emp.salary);
     
    	printf("%s\n"   ,emp.name);
    	printf("%d\n"     ,emp.empId);
    	printf("%.f\n",emp.salary);
   	return 0;
	}
**14). Coding competition**

	#include<stdio.h>
	int main()
	{
    	char str1[50];
    	char *ptr;
    	int  ctrV,ctrC;
    	fgets(str1, sizeof str1, stdin);
    	ptr=str1;
    	ctrV=ctrC=0;
    	while(*ptr!='\0'){
    	if(*ptr=='A' ||*ptr=='E' ||*ptr=='I' ||*ptr=='O' ||*ptr=='U' ||*ptr=='a' ||*ptr=='e' ||*ptr=='i' ||*ptr=='o' ||*ptr=='u')
    	ctrV++;
    	else
    	ctrC++;
    	ptr++; }
    	printf("%d %d",ctrV,ctrC-0);        
    	return 0;
	}
**15). Fee structure**

	#include<stdio.h>
	union Student
	{ 
	int roll,fees;
	char name[20],course[20];
	};
	int main()
	{
		union Student s1;
		printf("Details of student\n");
		scanf("%d",&s1.roll);
		printf("Roll Number=%d\n",s1.roll);
		scanf("%s",s1.name);
		printf("Name=%s\n",s1.name);
		scanf("%s",s1.course);
		printf("Course=%s\n",s1.course);
		scanf("%d",&s1.fees);
		printf("Fees=%d\n",s1.fees);
    		return 0;
	}
**16). Word stem**

	#include <stdio.h>
	#include<string.h>
	int main()
	{
		int i,j,k,l,m,n,o,p,t,len[15],flag,s,z,key,min;
		char a[15][25],ans[25],aa[25];
		scanf("%d",&t);
		for(z=1;z<=t;z++)
		{
			flag=s=0;
			min=1000;
			for(i=0;i<=24;i++)
			{
				ans[i]='\0';
			}
			scanf("%d",&n);
			for(i=0;i<=n-1;i++)
			{
			scanf("%s",a[i]);
			m=strlen(a[i]);
			len[i]=m;
			if(m<min)
			{
				min=m;
				key=i;
			}
		}
		for(i=min;i>=1;i--)
		{
		for(j=0;j<=min-i;j++)
		{
			 l=j;
			 k=0;
			while(k<=i-1)
			{
				aa[k]=a[key][l];
				k++;
				l++;
			 }
			aa[k]='\0';
		 	for(o=0;o<=n-1;o++)
			{
				flag=0;
				for(p=0;p<=len[o]-i;p++)
				 {
					if(strcmp(&a[o][p],aa)==a[o][p+i])
					{
						 flag=1;
						 break;
					}
         			  }
				 if(flag==0)
				  break;
			 }
			if(flag==1)
			{
				s=1;
				if(strlen(ans)==0)
				{
					strcpy(ans,aa);
				}
				else
				 {
            				if(strcmp(ans,aa)>0)
					strcpy(ans,aa);
				  }
			}
		 }
		if(s==1)
		break;
	}
	printf("%s\n",ans);
     }
     return 0;
    }
    

