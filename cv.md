<html>
<h1>Maksim Sviridov</h1>
<h2>phone number: </h2> +375297274460
<h3>About myself: There is an idea that the theory and practice in the college where I study is not enough to find a full-fledged job as a programmer. I am taking this course on the advice of a friend. I am a positive person and if I get down to business, then only circumstances from the outside can prevent me from doing it. I hope I can join this process, because for me the most difficult thing is to start to understand. I think the reason for this is the meager theoretical and practical experience. There is not much experience in writing code in Delphi.
<h2>Code example: </h2>
program Project11;  
uses  
SysUtils;  
type cheloveki = record  
name:string;  
age:integer;  
zp:extended;  
end;  
var  
v:string;  
i,j,count,n,min,p,i1,j1,d1,agez,voz,zarp:integer;  
f1,f2,f3:textfile;  
nl,nr,z,x:integer;  
count1,zpz:extended;  
f,b,nm:integer;  
s,e0,e1,e2:string;  
chel:array[1..4] of cheloveki;  
procedure vvod;  
begin  
count := 0;  
while count < 4 do  
begin  
count := count+1;  
writeln('Введите имя ',count,'-го сотрудника ');  
read(chel[count].name);  
writeln('Введите возраст ',count,'-го сотрудника ');  
read(chel[count].age);  
writeln('Введите зарплату ',count,'-го сотрудника ');  
readln(chel[count].zp);  
end;  
end;  

procedure sort1;  
begin  
for i := 1 to 4 do  
begin  
min:=i;  
for j := i+1 to 4 do  
if (chel[j].name<chel[min].name) then  
min:=j;  
s:=chel[i].name;{имя} agez:= chel[i].age;{возраст} zpz:= chel[i].zp; {зарплата}  
chel[i].name:=chel[min].name; {} chel[i].age:=chel[min].age; {} chel[i].zp:=chel[min].zp;  
chel[min].name:=s; {} chel[min].age:=agez; {} chel[min].zp:=zpz;  
end;  
writeln('Отсортированные имена: ');  
for i := 1 to 4 do  
begin  
e1:= floattostr(int(chel[i].zp));  
e2:= floattostr(frac(chel[i].zp));  
delete(e2,1,1);  
e0:=e1+e2;  
writeln(chel[i].name,' ', chel[i].age,' ',e0);  
end;  
readln;  
end;  
</h3>
</html>