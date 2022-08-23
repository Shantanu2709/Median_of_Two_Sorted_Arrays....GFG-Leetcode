# Median_of_Two_Sorted_Arrays....GFG-Leetcode
static double median(int arr1[],int arr2[])
{
int n=arr1.length;
int m=arr2.length;
//creating a new array of size (n+m)
int new_arr[] = new int[n+m];
int i=0,j=0,k=0;
int size =(n+m)/2;
while(k<=new_arr.length && i<n && j<m)
{
if(arr1[i]<arr2[j])
{
  new_arr[k++] = arr1[i++];
  }
  else
  {
  new_arr[k++] = arr2[j++];
  }
  }
  while(k<=new_arr.length && i<n)
  {
  new_arr[k++]=arr1[i++];
  }
  while(k<=new_arr.length && i<n)
  {
  new_arr[k++]=arr2[j++];
  }
  if((n+m)%2==0)
  {
    return ((double) new_arr[size]+new_arr[size-1])/2;
    }
    else
    {
    return (double) new_arr[size];
    }
    }
