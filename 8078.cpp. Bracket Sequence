#include <bits/stdc++.h>
#define ll long long int
#define pb push_back
#define IOS ios::sync_with_stdio(0); cin.tie(0); cout.tie(0);
#define pi acos(-1)
#define N 1000000
using namespace std;
int main()
{
    IOS
    ll t;
    cin>>t;
    for(ll i=1; i<=t; i++){
        string br;
        cin>>br;
        stack<char>st;
        stack<ll>ans, track;
        for(ll j=br.size()-1, k=0, l=1; j>=0; j--, k=0, l++){
            if(st.empty()){
                st.push(br[j]);
                track.push(j);
                ans.push(0);
            }
            else{
                char ch=st.top();
                if(br[j]=='(' && ch==')' ){ st.pop(); track.pop(); }
                else if(br[j]=='{' && ch=='}' ){ st.pop(); track.pop(); }
                else if(br[j]=='[' && ch==']' ){ st.pop(); track.pop(); }
                else if(br[j]=='<' && ch=='>' ){ st.pop(); track.pop(); }
                else{
                    st.push(br[j]);
                    track.push(j);
                    ans.push(0);
                    k=5;
                }
                if(k==0){
                    if(track.empty())ans.push(l);
                    else ans.push(track.top()-j);
                }
            }

        }
        cout<<"Case "<<i<<":"<<endl;
        while(!ans.empty()){cout<<ans.top()<<endl; ans.pop(); }

    }


    return 0;
}
