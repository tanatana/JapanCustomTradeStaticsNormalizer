# JapanCustomTradeStaticsNormalizer

A simple normalizer for Japan custom trade statics.

## Usage

```sh
trade-statics-normalizer [flags] CSV_FILES...

Flags:
  -h, --help         help for trade-statics-normalizer
  -o, --out string   Outpu file name. Default is STDOUT.
```

## Installation

```sh
go install github.com/tanatana/trade-statics-normalizer
```

## Example

### Input

```
Exp or Imp,Year,HS,Unit1,Unit2,Quantity1-Year,Quantity2-Year,Value-Year,Quantity1-Jan,Quantity2-Jan,Value-Jan,Quantity1-Feb,Quantity2-Feb,Value-Feb,Quantity1-Mar,Quantity2-Mar,Value-Mar,Quantity1-Apr,Quantity2-Apr,Value-Apr,Quantity1-May,Quantity2-May,Value-May,Quantity1-Jun,Quantity2-Jun,Value-Jun,Quantity1-Jul,Quantity2-Jul,Value-Jul,Quantity1-Aug,Quantity2-Aug,Value-Aug,Quantity1-Sep,Quantity2-Sep,Value-Sep,Quantity1-Oct,Quantity2-Oct,Value-Oct,Quantity1-Nov,Quantity2-Nov,Value-Nov,Quantity1-Dec,Quantity2-Dec,Value-Dec
2,2023,'000000011',  ,KG,0,1917608,831854,0,87030,39506,0,72114,34952,0,135866,41532,0,212472,73405,0,174017,94372,0,115162,61624,0,136110,67990,0,191268,83100,0,194132,81240,0,207532,64179,0,180077,93200,0,211828,96754,191268,83100,0,194132,81240,0,207532,64179,0,180077,93200,0,211828,96754
```

### Output

```
expOrImp,year,month,HS,data category,unit,value
2,2023,1,000000011,Quantity2,KG,87030
2,2023,2,000000011,Quantity2,KG,72114
2,2023,3,000000011,Quantity2,KG,135866
2,2023,4,000000011,Quantity2,KG,212472
2,2023,5,000000011,Quantity2,KG,174017
2,2023,6,000000011,Quantity2,KG,115162
2,2023,7,000000011,Quantity2,KG,136110
2,2023,8,000000011,Quantity2,KG,191268
2,2023,9,000000011,Quantity2,KG,194132
2,2023,10,000000011,Quantity2,KG,207532
2,2023,11,000000011,Quantity2,KG,180077
2,2023,12,000000011,Quantity2,KG,211828
2,2023,1,000000011,Value,,39506
2,2023,2,000000011,Value,,34952
2,2023,3,000000011,Value,,41532
2,2023,4,000000011,Value,,73405
2,2023,5,000000011,Value,,94372
2,2023,6,000000011,Value,,61624
2,2023,7,000000011,Value,,67990
2,2023,8,000000011,Value,,83100
2,2023,9,000000011,Value,,81240
2,2023,10,000000011,Value,,64179
2,2023,11,000000011,Value,,93200
2,2023,12,000000011,Value,,96754
```

## Feature

- normalize
- omit empty data

## Where you have to go to get the original Trade Statics data

https://www.e-stat.go.jp/stat-search/files?page=1&layout=datalist&toukei=00350300&tstat=000001013141&cycle=1&tclass1=000001013183&tclass2=000001013185&tclass3val=0&metadata=1&data=1

## When you need to know more detail of the CSV specification

https://www.customs.go.jp/toukei/sankou/howto/faq.htm

If you know more better documentation, please tell me :)
