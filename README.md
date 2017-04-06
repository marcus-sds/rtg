# rtg

## db table creation

## switch add

## start rtg

## update switch

## cron registration
0,5,10,15,20,25,30,35,40,45,50,55 * * * * su - root -c "cd /app/rtg/html/rtg;/usr/bin/php /app/rtg/html/rtg/intStat-5m.php > /dev/null 2>&1"
