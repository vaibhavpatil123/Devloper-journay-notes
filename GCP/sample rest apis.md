https://cloud.google.com/storage/docs/xml-api/put-bucket-lifecycle#request_body_elements
PUT /example.com?lifecycle HTTP/1.1
Host: storage.googleapis.com
Content-Length: 220
Authorization: Bearer ya29.AHES6ZRVmB7fkLtd1XTmq6mo0S1wqZZi3-Lh_s-6Uw7p8vtgSwg

<?xml version="1.0" ?>
<LifecycleConfiguration>
    <Rule>
        <Action>
            <Delete/>
        </Action>
        <Condition>
            <Age>30</Age>
        </Condition>
    </Rule>
</LifecycleConfiguration>



https://cloud.google.com/resource-manager/docs/access-control-org



Request:

POST https://cloudresourcemanager.googleapis.com/v1/organization/12345:testIamPermissions

{
    "permissions":  [
        "resourcemanager.organizations.get",
        "resourcemanager.organizations.setIamPolicy"
    ]
}

Response:

{
    "permissions": [
        "resourcemanager.organizations.get"
    ]
}
