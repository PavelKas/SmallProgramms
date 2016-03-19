#include "stdafx.h"
#include <iostream>

using namespace std;

int main()
{
	int a[5];
	int min,z=0;
	for (int i = 0; i < 5; ++i)
	{
		cout << i + 1 << ": ";
		cin >> a[i];
	}
	for (int l = 0; l < 5; ++l)
	{
		min = a[l];
		for (int k = l; k < 5; ++k)
		{
			if (a[k] < min)
			{
				min = a[k];
				z = k;
			}
		}
		if (z != 0)
		a[z] = a[l];
		a[l] = min;
		z = 0;
	}
	for (int i = 0; i < 5; ++i)
		cout << a[i] << " ";
	system("pause");
	return 0;
}