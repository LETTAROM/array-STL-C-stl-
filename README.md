//# array-STL-C-stl-
//array STL Обучение C++   Библиотека стандартных шаблонов(stl)
#include<array>
  using namespace std;
int main()
{
	array<int, 4>arr = { 5,9,8 }; // array<int, 4>arr;
	cout<<arr[0] << endl;
	
	try
	{
cout << arr.at(11) << endl;//проверяет размер массива исообщит если б попытка выйти за границы памяти
	//т е б. бросать исключения
	}
	catch (const std::exception&ex)
	{
		cout << ex.what() << endl;
	}
	for (int i = 0; i < arr.size(); i++)//возвр. кол-во эл-в
	{
		cout << arr[i] << endl;
	}

	for (auto el:arr)//см 137
	{
		cout << el << endl;
	}
	arr.fill(-1);
	for (auto el : arr)//см 137
	{
		cout << el << endl;
	}
	cout << "/////////////////////" << endl;
	cout << arr.front() << endl;//доступ к 1 эл-ту массива
	cout << arr.back() << endl;//доступ к последнему  эл-ту массива
	   	 
	return 0;
}
