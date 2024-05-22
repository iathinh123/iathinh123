- 👋 Hi, I’m @iathinh123
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
#include<conio.h>
#include<iostream>
#include<stdlib.h>
#include <queue>
using namespace std;
struct khohang
{
	char NXS[15];//nguoi san xuat
	char NTD[15];//nguoi tieu dung
	int mat_hang;
};
struct qnode
{
	khohang info;
	qnode* next;
};
struct qlist
{
	qnode* head;
	qnode* tail;
};
void taolist(qlist q)
{
	q.head = NULL;
	q.tail = NULL;
}
qnode* taonut(khohang x)
{
	qnode* p = new qnode;
	if (p == NULL)
	{
		cout << "Khong the cap node" << endl;
		return NULL;
	}
	p->info = x;
	p->next = NULL;
	return p;
}
int ktra_rong(qlist& q)
{
	if (q.head == NULL)
		return 1;
	else
		return 0;
}
int themcuoi(qlist& q, qnode* p)
{
	if (p == NULL)
		return 0;
	if (ktra_rong(q) == 1)
	{
		q.head = p;
		q.tail = p;
	}
	else
	{
		q.tail->next = p;
		q.tail = p;
	}
	return 1;
}
int xoaqueue(qlist& q, khohang& x)
{
	if (ktra_rong(q) == 1)
		return 0;
	qnode* p = q.head;
	q.head = q.head->next;
	if (q.head == NULL)
		q.tail = NULL;
	x = p->info;
	delete p;
	return 1;
}
int thongtin(qlist q,khohang&x)
{
	if (ktra_rong(q) == 1)
		return 0;
	x = q.head->info;
	return 1;
}
int cau1(khohang& x)
{
	int n;
		cout << "so luong mat hang vao kho: " << endl;
		cin >> n;
		if (n <= 0)
		{
			cout << "so luong mat hang phai lon hon 0" << endl;
			return 1;
		}

}

int cau2(qlist q,int n)
{
	for (int i = 0; i < n; i++)
	{
		if (ktra_rong(q) == 1)
			return 0;
		else
		{
			int dem = 1;
			qnode* p = q.head;
			while (p != NULL)
			{
				cout << "Thong tin mat hang: " << endl;
				dem++;
				p = p->next;
			}
		}
		return 1;
	}
}

//int cau3(qlist q,khohang &x)
//{
//	if (ktra_rong(q) == 1)
//		return 0;
//	while (q.head != NULL)
//	{
//		x = q.head->info;
//	}
//}
void menu()
{
	cout << "**********" << endl;
	cout << "***MENU***" << endl;
	cout << "Cau 1" << endl;
	cout << "cau 2" << endl;
}
void main()
{
	menu();
	qlist q;
	khohang x;
	qnode* p;
	qnode* q;
	taolist(q);
	int n;
	int luachon;
	do
	{
		cout << "Nhap lua chon" << endl;
		cin >> luachon;
		switch (luachon)
		{
		case 1:
		{
			int n;
			cout << "Nhap so mat hang:" << endl;
			cin >> n;

		}
		}
	} while (luachon != 0);
}
<!---
iathinh123/iathinh123 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
