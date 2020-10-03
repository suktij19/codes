# codes
//atRto TLH
#include<bits/stdc++.h>
using namespace std;
#define IOS ios_base::sync_with_stdio(false);cin.tie(NULL)
#define pb push_back
#define ll long long
const ll MOD = 1e9+7;
#define ln '\n'
#define all(x) (x).begin(), (x).end()
#define rotate rotate(vec.begin(), vec.begin() + k, vec.end())
#define alloc(v) set<int> S(all(v))
#define bitset(n)  bitset<20>(n)
#define Min min({a, b, c, d})
 #define CLOCK cerr << "\nTime elapsed: " << 1000 * clock() / CLOCKS_PER_SEC << "ms\n";
 
    const ll INF=150000000;
    char ch[1003][1003];
 
    ll vis[1002][1002];  
    ll size=0;
    ll dp[100007];
   
   
 
   void solve(){
 
   }
     
 
 
    int main() {
      IOS;
       #ifndef ONLINE_JUDGE
     freopen("input.txt","r",stdin);
     freopen("output.txt","w",stdout);
     #endif
	 
	 ll tt;
	 cin>>tt;
	 while(tt--){
	 	
      ll n;
      cin>>n;
      ll a[n];
      vector<ll>v(100,-1);
      vector<ll>v1(100,-1);
      map<ll,ll>mp;
      for(ll i=0;i<n;i++){
        cin>>a[i];
        mp[a[i]]++;
      }
      ll ans=0,k=0,m=0;
      for(auto i:mp){
      	if(i.second>1){
      		v[k]=i.first;
      		v1[m]=i.first;
      		k++;
      		m++;
      	}
      	else{
      		v[k]=i.first;
      		k++;
      	}
      }
      //sort(all(v));
      //sort(all(v1));
      for(ll i=0;i<=100;i++){
      	if(v[i]!=i){
      	
      		ans+=i;
      		//cout<<ans<<ln;
      		break;
      	}
       }
       //cout<<ln;
       for(ll i=0;i<=100;i++){
      	if(v1[i]!=i){
      	
      		ans+=i;
      		//cout<<ans<<ln;
      		break;
      	}
       }
       cout<<ans<<ln;
    }
    CLOCK;
    return 0;
 }
