## IDEAS
1. To communicate with HubSpot Contacts API.
2. There are more than 10 endpoints for each specific tasks by HubSpot. However, I find that create, update and delete contact are most commonly used.
3. Also, HubSpot required certain standards in order to store date via Contacts API. I have written the function "expiry_timestamp" (can be found under utils.py) which suits my case to update the expiration date. That would be a reference for you if you want to code functions which suit your tasks.

## LOGICS
***Notes: Check out app.py for reference***

**1. Create or Update Contact**
```
findRecord = get_contact_by_email
if findRecord:
    update_property
else:
    create_contact
```

**2. Delete Contact**
```
findRecord = get_contact_by_email
if findRecord:
    del_contact
```

## INSTRUCTIONS
**Step 1(a)**
```
Setup a virtual environment
```

**Step 1(b): pip install required packages**
```
pip install -r requirements.txt
```

**Step 2: Create a .env file and included the following environment variables to this file**
```
HUBSPOT_KEY=yourHubSpotAPIKey
HUBSPOT_ENDPOINT=https://api.hubapi.com/contacts/v1/contact
```

## CHANGELOG
***Notes: Example can be found on app.py***
##### _version 1.0.0_
- Updated at: Dec 21, 2020 02.20AM GMT+8
- Methods for HubSpot Contact APIs
    - get_contact_by_email
    - create_contact
    - update_property
    - del_contact
- These functions allow users to get and post data from/to HubSpot