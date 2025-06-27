# ACI Deployment Role

This role deploys a Cisco ACI Tenant along with its VRF, Application Profiles, Bridge Domains, Subnets, and EPGs. It is designed for use with AWX/Tower and accepts survey inputs as variables.

## Variables

- `aci_tenant`: Name of the Tenant
- `aci_vrf`: Name of the VRF under the tenant
- `aci_app_profiles`: Comma-separated string of application profiles
- `aci_bridge_domains`: Comma-separated string of bridge domains
- `aci_subnets`: JSON list of subnets with `bd`, `gateway`, `mask`, `scope`
- `aci_epgs`: JSON list of EPGs with `name`, `app_profile`, `bd`

