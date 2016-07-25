# BashFlu

##bashFlu

## Find recently installed packages 
rpm -qa --queryformat '%{installtime} %{name}-%{version}-%{release} %{installtime:date}\n' | sort -nr +1 | sed -e 's/^[^ ]* //'
