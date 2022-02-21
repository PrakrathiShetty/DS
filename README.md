#include<iostream><br>
using namespace std;<br>
struct Node{<br>
	int value;<br>
	struct Node *next;<br>
};<br>
struct Node* head=NULL;<br>
struct Node* sHead=NULL;<br>
struct Node* temp=NULL;<br>
void insert(int new_data){<br>
	struct Node* new_node=new Node();<br>
	new_node->value=new_data;<br>
	new_node->next=head;<br>
	head= new_node;<br>
}<br>
int n;<br>
int ele;<br>
int splitIndex;<br>
int main ()<br>
{<br>
	int i;<br>
	cout<<"enter number of elements you want in the list \t";<br>
	cin>>n;<br>
	cout<<"enter elements:"<<endl;<br>
	for(i=0;i<n;i++)<br>
	{<br>
	cin>>ele;<br>
	insert(ele);<br>
	}<br>
cout<<"\n list of elements:"<<endl;<br>
Node *t;<br>
t=head;<br>
while(t!=NULL)<br>
{<br>
	cout<<t->value<<"\t";<br>
	t=t->next;<br>
}<br>
cout<<"\n enter the position you want the list to split";<br>
cin>>splitIndex;<br>
while(splitIndex<0||splitIndex>n-1)<br>
{<br>
	cout<<"invalid position.try again"<<endl;<br>
	cin>>splitIndex;<br>
}<br>
temp=head;<br>
for(i=0;i<splitIndex;i++)<br>
{<br>
	if(i==splitIndex-1)<br>
	{<br>
	Node *tN;<br>
	tN=temp->next;<br>
	sHead=tN;<br>
	temp->next=NULL;<br>
	break;<br>
	}<br>
	temp=temp->next;<br>
}<br>
temp=head;<br>
if(temp==NULL)<br>
{<br>
cout<<"\n first list is empty"<<endl;<br>
}<br>
else<br>
{<br>
	cout<<"\nfirst list element"<<endl;<br>
	while(temp!=NULL)<br>
	{<br>
		cout<<temp->value<<"\t";<br>
		temp=temp->next;<br>
	}<br>
}<br>
temp=sHead;<br>
if(temp==NULL)<br>  
{<br>
	cout<<"\nsecomd list is empty"<<endl;<br>
}<br>
else<br>
{<br>
	cout<<"\n\n second list element"<<endl;<br>
	while(temp!=NULL)<br>
	{<br>
		cout<<temp->value<<"\t";<br>
		temp=temp->next;<br>
	}<br>
}<br>
return 0;<br>
}
<br>
<br>
<br>
 <br>
  ![image](https://user-images.githubusercontent.com/99945753/154906391-e29f59d6-51a7-44e4-9681-ad3cbd24ed1f.png)<br>
