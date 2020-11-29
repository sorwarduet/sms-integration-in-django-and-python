# sms-integration-in-django-and-python

# First install urllib3

```
(venv) $ pip install urllib3
```
Now import package in project

```
contact ='+8801621757014' # contact number
message = 'Hi, I am form DUET TEST' # message
sms = SmsSystem()  # creae obj
sms.sent_sms(contact,message) # call from sent class or others

class SmsSystem:

    def sent_sms(self, contact, msg):
        http = urllib3.PoolManager()
        r = http.request('GET','http://isms.zaman-it.com/smsapi?api_key=APIKey&type=text&contacts='+contact+'&senderid=8809612451697&msg='+msg)
        print(r)


```
