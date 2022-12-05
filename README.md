# dizideki-sayilari-küçükten-büyüğe-siralama

#include<stdio.h>
int main(void)
{
	int dizi[50],gecici,adet,i,j;
	printf("kac adet sayi girilecek");
	scanf("%d",&adet);
	
	for(i=0;i<adet;i++) //kullanicidan sayilari aliyoruz
	{
		printf("%d)sayiyi giriniz",i+1);
		scanf("%d",&dizi[i]);
	}
	for(i=0;i<adet-1;i++)
	{
		for(j=i+1;j<adet;j++)
		{
			if(dizi[i]>dizi[j])
			{
				gecici=dizi[i];
				dizi[i]=dizi[j];
				dizi[j]=gecici;
			}
		}
	}
	for(i=0;i<adet;i++)
	{
		printf("%d",dizi[i]);
		printf("\n");
	}
	return 0;
}
