
# Starting Mock Server

- docker build -t zenvia-api-mock .
- docker run -p 8080:8080 zenvia-api-mock


# Mock rules

- Authorization: "user:pass"
- Number 5551999999200 always return HTTP Code Status OK(200) with a success payload


# Call api-rest / send-sms with a valide request 

- curl -v --user "user:pass" -H "Accept: application/json" -H "Content-Type: application/json" -X POST -d '{"sendSmsRequest": { "from": "Remetente", "to": "5551999999200", "schedule": "2017-08-09T14:00:00", "msg": "SMS Message", "callbackOption": "NONE", "id": "msg-id",  "aggregateId": "14828", "flashSms": true}}' http://localhost:8080/api-rest/services/send-sms
