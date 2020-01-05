## env
region="eu-west-1"
## Zlozenia
Budowana jest aplikacja.  
Aplikacja dziala na wirtualnej maszynie i  musi miec mozliwosc zapisywanie na bucket S3.  

## Wymagania
1. Mozliwosc zapisu przez applikacje do s3 bucket.  
2. Mozliwosc wylistowania zawarosci w celu okreslenia czy zawartosci bucket.

## Utworzenie Bucket
'''
aws2 s3api create-bucket --bucket hw-week3 --region $region \
    --create-bucket-configuration LocationConstraint=$region
'''