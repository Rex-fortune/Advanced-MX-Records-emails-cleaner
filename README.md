# Advanced-MX-Records-emails-cleaner

FOR LEGITIMATE USE CASE ONLY!!! This scripts removes all bad emails, duplicated addresses, dead domains of emails, spyware emails to catch scrapped emails, email addresses with invalid mx records and sometimes in valid smtp records.

it will make your email list 85% cleaner than before.

FRAMEWORK
This script is built using python. make sure you have python installed.

Usage:
     USING IT AS ONLY MX-RECORDS VERIFIER
        It can be used to filter out both bad mx-records and bad smtp records. Note that regardless of if you use it for only MX record verifier only  or both, It will filter out duplicates, bad domains, invalid email addresses, abandoned email addresses. 
        You need to have a strong sender domain to verify smtp records else, sending of emails to test for smtp after sometime will return null and it will judge both good        and bad emails as bad.
        If  u want an aggressive filtering increase the workers numbers.

  USING IT AS ONLY MX-RECORDS VERIFIER
  python smtp_peek_emails.py --list emails_to_be_cleaned.txt --workers 10 --skip-smtp --output cleaned_emails.txt
  python smtp_peek_emails.py --list emails_to_be_cleaned.csv --workers 10 --skip-smtp --output cleaned_emails.csv

  USING IT AS ONLY MX-RECORDS AND SMTP VERIFIER
  python smtp_peek_emails.py --list emails_to_be_cleaned.txt --workers 10 --output cleaned_emails.txt
  python smtp_peek_emails.py --list emails_to_be_cleaned.csv --workers 10 --output cleaned_emails.csv

External Dependencies: None (uses only Python standard library)
  pip install dnspython
