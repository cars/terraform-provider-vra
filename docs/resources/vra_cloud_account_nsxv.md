---
page_title: "VMware Aria Automation: vra_cloud_account_nsxv"
description: |-
    Creates a vra_cloud_account_nsxv resource.
---

# Resource: vra_cloud_account_nsxv

Creates a VMware Aria Automation NSX-V cloud account resource.

## Example Usages

The following example shows how to create an NSX-V cloud account resource.

```hcl
resource "vra_cloud_account_nsxv" "this" {
  name        = "tf-NSX-V-account"
  description = "foobar"
  username    = var.username
  password    = var.password
  hostname    = var.hostname
  dc_id       = var.vra_data_collector_id

  accept_self_signed_cert = true

  tags {
    key   = "foo"
    value = "bar"
  }
}
```

## Argument Reference

Create your NSX-V cloud account resource with the following arguments:

* `accept_self_signed_cert` - (Optional) Accept self-signed certificate when connecting to the cloud account.

* `dc_id` - (Optional) Identifier of a data collector VM deployed in the on premise infrastructure.

* `description` - (Optional) Human-friendly description.

* `hostname` - (Required) Host name for NSX-V cloud account.

* `name` - (Optional) Name of NSX-V cloud account.

* `password` - (Required) Password used to authenticate to the cloud account.

* `tags` - (Optional) Set of tag keys and values to apply to the cloud account. Example: [ { "key" : "vmware", "value": "provider" } ]

* `username` - (Required) Username used to authenticate with the cloud account.

## Attribute Reference

* `associated_cloud_account_ids` - Cloud accounts associated to the cloud account.

* `created_at` - Date when entity was created. Date and time format is ISO 8601 and UTC.

* `id` - ID of NSX-V cloud account.

* `links` - Hypermedia as the Engine of Application State (HATEOAS) of entity.

* `org_id` - ID of organization that entity belongs to.

* `owner` - Email of entity owner.

* `updated_at` - Date when entity was last updated. Date and time format is ISO 8601 and UTC.

## Import

To import the NSX-V cloud account, use the ID as in the following example:

`$ terraform import vra_cloud_account_nsxv.new_gcp 05956583-6488-4e7d-84c9-92a7b7219a15`
