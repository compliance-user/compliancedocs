<h1 style="color:rgb(30 215 96)">Compliance MyStandard Creation</h1>
<h5 style="color:rgb(25 20 20);">To create a new compliance my-standard, you will need a json file and an excel file. The Json file is used for creating a standard and the excel file is used for creating compliance controls along with policy mapping through bulk upload option from the UI</h5>



<h4 style="color:rgb(30 215 96)">Sample Json for creating a compliance standard</h4>

```json
{
    "control_action_attributes": {
        "action_method": {
            "optional": false,
            "ui-text-element": "dropdown",
            "allowed_values": [
                "Report",
                "Policy",
                "Document",
                "Validation",
                "Monitoring"
            ],
            "filter": false,
            "position": 5,
            "label": "Control action method",
            "type": "string"
        },
        "nature": {
            "optional": false,
            "ui-text-element": "dropdown",
            "allowed_values": [
                "Manual",
                "Automated"
            ],
            "filter": true,
            "position": 2,
            "label": "Control action nature",
            "type": "string"
        },
        "purpose": {
            "optional": false,
            "ui-text-element": "dropdown",
            "allowed_values": [
                "Preventive",
                "Detective"
            ],
            "filter": false,
            "position": 3,
            "label": "Control action purpose",
            "type": "string"
        },
        "classification": {
            "optional": false,
            "ui-text-element": "dropdown",
            "allowed_values": [
                "Technical",
                "Process"
            ],
            "filter": false,
            "position": 4,
            "label": "Control action classification",
            "type": "string"
        },
        "level": {
            "optional": false,
            "ui-text-element": "dropdown",
            "allowed_values": [
                "Account",
                "Workload",
                "Cloud account",
                "Organization",
                "Resource",
                "OS"
            ],
            "filter": true,
            "position": 1,
            "label": "Control action level",
            "type": "string"
        }
    },
    "control_attributes": {
        "Control_Clause": {
            "type": "string",
            "ui-text-element": "text-area",
            "label": "Security Category",
            "abstracted-name": "Subcategory",
            "filter": true,
            "position": 2,
            "optional": true
        },
        "Category": {
            "type": "string",
            "ui-text-element": "dropdown",
            "label": "Security Category",
            "abstracted-name": "Category",
            "filter": true,
            "position": 2,
            "allowed_values": [
                "1. Identity and Access Management",
                "2. Security Center",
                "3. Storage Accounts",
                "4. Database Services",
                "5. Logging and Monitoring",
                "6. Networking",
                "7. Virtual Machines",
                "8. Other Security Considerations",
                "9. App Service"
            ],
            "optional": false
        },
        "Control": {
            "type": "string",
            "ui-text-element": "text-area",
            "label": "Control Objective",
            "filter": false,
            "position": 3,
            "abstracted-name": "Control Name",
            "purpose": "compliance_control_name",
            "optional": false
        },
        "description": {
            "type": "string",
            "ui-text-element": "text-area",
            "label": "Description",
            "filter": false,
            "position": 4,
            "optional": false
        }
    }
}
```

This <a href="https://onedrive.live.com/edit.aspx?action=editnew&resid=88EBB5A04CE01D0!108&ithint=file%2cxlsx&action=editnew&wdNewAndOpenCt=1634739785662&wdPreviousSession=44602f5f-844f-4eae-b1d3-bd51506a69e8&wdOrigin=OFFICECOM-WEB.START.NEW">Excel link</a> is used for creating compliance controls and policy mapping.

<b>All the json fields should be matched with excel document. If they are not matched then you will get a validation error in the UI</b>

<b>Allowed values inside each attribute should also be matched the same in the excel sheet.</b> 



<h5>Support and Maintenance</h5>

---

<h6>Name: Siva K</h6>

<h6>Email: siva@corestack.io</h6>

----

<h6>Name: Siva M</h6>

<h6>Email: siva.m@corestack.io</h6>

---

<h6>Thanks,</h6>

<b>Compliance-Team</b>

