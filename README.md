# 农历与新历互转
农历转新历，新历转农历
获得某年的生肖，获取农历某月的总天数
农历某天从春节至今的天数
## 安装

> composer require since/lunar dev-master 

### 调用例子
```
use since\Lunar;
class Index
{


    public function index(){
        $lunar=new Lunar();
        //农历转新历，当这个月是闰月时，第四个参数为true
        $lunar->convertLunarToSolar('2020','06','01');//
        //新历转农历
        $lunar->convertSolarToLunar('2020','06','01');//
        //某个月的所有新历与农历数据，当传第三个参数日期时，返回当天的新历与农历数据
        $arr=$lunar->convertSolarMonthToLunar("2020",'06');
        //判断某年是不是闰年
        $lunar->isLeapYear(2020);
        //获得某年的生肖
        $lunar->getYearZodiac(2020);
        //获取农历某月的总天数
        $lunar->getLunarMonthDays(2020,01);
        //获取某年的所有月份的天数
        $lunar->getLunarMonths(2019);
        //获取农历某年的总天数
        $lunar->getLunarYearDays(2020);
        //获得某年的闰月
        $lunar->getLeapMonth(2020);
        //农历某天从春节至今的天数，传农历日期，当这个月是闰月时，第四个参数为true，当这个月是闰月时，第四个参数为true
        $lunar->getDaysBetweenLunar(2020,07,15);
        //两个日期至今相隔天数
        $lunar->getDaysBetweenSolar(2020,06,02,05,01);
    }
}
```
