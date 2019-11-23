# second-repo
Program checks if panagram or not

import java.util.Scanner;

class Main{
public static void main(String args[])
{
Scanner s = new Scanner(System.in);
System.out.println("Enter String1");
String s1 = s.nextLine();
System.out.println("Enter STring2");
String s2 = s.nextLine();

boolean rs = isPanagram(s1, s2);

if(rs)
System.out.println("Strings are panagrams");
else
System.out.println("Are not panagrams");
}

private static boolean isPanagram(String s1)
{
if(s1.length()<26)
return false;

int count[] = new int[26];

for(int i = 0; i<s1.length(); i++)
{
char ch = s1.charAt(i);
if(ch>='A' && ch<='Z')
{
count[ch-65]++;
}
else if(ch>='a'&& ch<='z')
{
count[ch-97]++;
}
}
for(int i = 0; i<count.length; i++)
{
if(count[i]==0)
{
return false;
}
return true;
}
}
