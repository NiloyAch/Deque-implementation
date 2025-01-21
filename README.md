

#include<bits/stdc++.h>
using namespace std;

typedef long long ll;
typedef double dl;

#define endl "\n"
#define optimize() ios_base::sync_with_stdio(0);cin.tie(0);cout.tie(0);
#define fraction() cout.unsetf(ios::floatfield); cout.precision(10); cout.setf(ios::fixed,ios::floatfield);
#define mem(a,b) memset(a, b, sizeof(a))

int main()
{
    optimize();
    deque<int> dq;

    int t;
    cin >> t;
    string s;

    while(t--)
    {
        cin >> s;
        if(s=="push_back")
        {
            int x;
            cin >> x;
            dq.push_back(x);
        }
        else if(s=="push_front")
        {
            int x;
            cin >> x;
            dq.push_front(x);
        }

        else if(s=="pop_front")
        {
            if(!dq.empty())
            {
                cout << dq.front() << endl;
                dq.pop_front();

            }
            else
            {
                cout << "Empty" << endl;
            }
        }
        else if(s=="pop_back")
        {
            if(!dq.empty())
            {
                cout << dq.back() << endl;
                dq.pop_back();
            }
            else
            {
                cout << "Empty" << endl;
            }
        }

    }
}
