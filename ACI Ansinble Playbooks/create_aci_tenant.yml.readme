### 📘 **Overview**
This playbook:
- Logs into the APIC
- Creates a tenant
- Is compatible with ACI v6.0(3e)
- Uses **Cisco ACI Ansible collection modules**

---

### 🧾 **Ansible Playbook: `create_aci_tenant.yml`**
```yaml
---
- name: Create Tenant in Cisco ACI
  hosts: localhost
  connection: local
  gather_facts: no
  collections:
    - cisco.aci

  vars_prompt:
    - name: apic_url
      prompt: "Enter APIC URL (e.g. https://apic.example.com)"
      private: no

    - name: username
      prompt: "Enter APIC username"
      private: no

    - name: password
      prompt: "Enter APIC password"
      private: yes

    - name: tenant_name
      prompt: "Enter Tenant Name"
      private: no

    - name: tenant_description
      prompt: "Enter Tenant Description"
      private: no

  tasks:
    - name: Create Tenant
      cisco.aci.aci_tenant:
        host: "{{ apic_url }}"
        username: "{{ username }}"
        password: "{{ password }}"
        tenant: "{{ tenant_name }}"
        description: "{{ tenant_description }}"
        use_ssl: yes
        validate_certs: no
        state: present
```

---

### ✏️ **Areas That Require Input**

| Variable           | Description                                     | Example                      |
|--------------------|--------------------------------------------------|------------------------------|
| `apic_url`         | URL of the APIC controller                       | `https://apic.example.com`   |
| `username`         | APIC login username                              | `admin`                      |
| `password`         | APIC password (hidden input)                     | *(your password)*            |
| `tenant_name`      | Name of the new tenant to create                 | `Dev_Tenant`                 |
| `tenant_description`| Description for the tenant                      | `Tenant for Dev Environment` |

---

### ✅ **Requirements**

- Ansible installed (`ansible-core`)
- Cisco ACI Ansible Collection:
  ```bash
  ansible-galaxy collection install cisco.aci
  ```

- Connectivity to APIC (network/firewall should allow access)

---

Would you like me to expand this with VRFs, Bridge Domains, or Contracts?
