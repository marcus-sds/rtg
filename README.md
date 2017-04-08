# rtg

## install rtg
prepare os with centos 6<br>

### install package
##### centos rtg install
yum install -y perl-devel<br>
yum install -y perl-DBI<br>
yum install -y perl-DBD-mysql<br>
yum install -y net-snmp<br>
yum install -y mysql-devel<br>
yum install -y net-snmp-devel<br>
yum install -y openssl-devel<br>

##### [option1] untar rtg.tar.gz file
download rtg.tar.gz<br>
mv rtg.tar.gz /usr/local<br>
tar xvfz rtg<br>

##### [option2] configure file modification and compile (4314 line)
<pre>
  str="$i/lib64/mysql/libmysqlclient.*"
  for j in `echo $str`; do
    if test -r $j; then
      MYSQL_LIB_DIR=$i/lib64/mysql
      break 2
    fi
  done

 5) rtg install
         $ gzip -d rtg-x.y.tar.gz
         $ tar -xvf rtg-x.y.tar
	 $ cd rtg-x.y/
         $ ./configure
	 $ make
	 # make install
</pre>

## db table creation

## switch add

## start rtg

## update switch

## prepare web

## cron registration
0,5,10,15,20,25,30,35,40,45,50,55 * * * * su - root -c "cd /app/rtg/html/rtg;/usr/bin/php /app/rtg/html/rtg/intStat-5m.php > /dev/null 2>&1"
