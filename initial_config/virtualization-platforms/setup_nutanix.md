# Nutanix setup

**Notice**: Nutanix environments require vProtect Node to be installed in one of the VMs residing on the Nutanix cluster. vProtect should detect automatically the VM with vProtect during index operation.

Please make sure to follow these steps: [LVM setup on vProtect Node for disk attachment backup mode](../setup_lvm.md)

When adding Nutanix HV managers \(Prism\) make sure to have URL like the following:

```text
https://PRISM_HOST:9440/api/nutanix/v3
```

Then index your HV manager and verify if hypervisors and VMs are detected.

**Notice**: volume groups attached to the VMs are **not** affected by snapshot, hence neither backup nor snapshot revert on such volumes is going to include them.

