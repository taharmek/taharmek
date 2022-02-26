### Hi there 👋

<!--
**taharmek/taharmek** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
--------------TIMER 1----------------

label1.left:=label1.left+1;
if label1.left=784 then
label1.left:=-512;



-----------progressbar------------------


if ProgressBar1.Position=100 then
begin
  Timer2.Enabled:=false;
  form2.show;
  form1.Hide;
end
else
Begin
 ProgressBar1.Position:=ProgressBar1.Position+1;
End;
----------Password---------------------------------------------------------------------


Adoquery1.SQL.Clear;
Adoquery1.SQL.Add ('select*from A1 where User='''+edit1.Text+''' and Password='''+edit2.Text+''' ');

Adoquery1.open;
if not Adoquery1.EOf then 
begin
form3.show;

form2.Hide;
end

else
messagedlg('Mot de passe incorrect', mterror,[mbok],0);

edit2.Clear;
end;
end.


--------------Button recherche----------------------


ADOTable1.Filter:='Num='+quotedstr(edit1.Text);
ADOTable1.Filtered:=true;

---------------Button Annuler la recherche-----------------------


ADOTable1.Filtered:=false;
