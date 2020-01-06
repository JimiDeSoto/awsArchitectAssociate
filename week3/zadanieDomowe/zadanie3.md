## env
region="eu-west-1"

## Zlozenia
Budowana jest aplikacja wspolp[arcujaca z s3 bucket.  
Aplikacja dziala na wirtualnej maszynie i musi miec mozliwosc zapisywanie na bucket S3.  

## Wymagania aplikacji pracujacej na vm
1. Mozliwosc zapisu  do s3 bucket.  
2. Mozliwosc wylistowania zawarosci w celu okreslenia zawartosci bucket.


## Procedura
1. Utworzenie policy umozliwiajacej wyswietlenie zawartosci bucket i umieszczenie tam pliku. allowBucketOp.json.
2. Utworzenie roli IAM dla serwisu EC2 z wczesniej utworzona polityka.
3. Dodanie nowej roli do maszyny wirtualnej.

## Utworzenie Bucket

aws2 s3api create-bucket --bucket hw-week3 --region $region \
    --create-bucket-configuration LocationConstraint=$region



# 1
## 2
### 3
#### 4
##### 5


