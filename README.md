# system-upadate
#!/bin/bash
This is a sytem update
N.B. Johnson
VERSION=$(cat /et/c*-release |grep release |head -1 |awk '{print $3}' |awk -F"." '{print $2})
if
[ $VERSION -lt 9 ]
then
echo -e "\n Updating the System\n"
yum update -y
else
echo -e "\n System is Up-To-Date\n"
fi
