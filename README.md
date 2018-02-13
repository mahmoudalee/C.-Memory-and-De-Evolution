# C.-Memory-and-De-Evolution

#include <iostream>

#include <algorithm>

using namespace std;

int main()
{

	int from, to, cnt = 0;
	cin >> from >> to;

	int arr[3] = { to,to,to };
	while (arr[0] != from || arr[1] != from || arr[2] != from)
	{
		sort(arr, arr + 3);
		arr[0] = arr[1] + arr[2] - 1;
		cnt++;
		if (arr[0] >= from)
			arr[0] = from;
	}
	cout << cnt << endl;
	return 0;
}
