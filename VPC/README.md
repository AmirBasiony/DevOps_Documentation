## AWS Cloud SAA-C03

- **Free Services**: VPCs, Subnets, IGW, VGW (`Virtual Private Gateway`), Routing Tables, ACLs.
- **VPC**:
    - The VPC address pool can be extended by adding up to 4 additional secondary CIDR blocks.

- **Route Table**:
    - After creating a **VPC**, a **Main Route Table** is created by default. This **Main Route Table** cannot be deleted.
    - When subnets are created within the VPC, the **Main Route Table** is automatically associated with these subnets by default.
    - **Custom route tables** can be created and attached to specific subnets. In this case, the **Main Route Table** will be automatically detached from those subnets.

- **Internet Gateway (IGW)**:
    - Managed by AWS.
    - Handles all inbound and outbound traffic between the VPC and the public internet.
    - Scales horizontally based on traffic workload.
- **Subnet**:
    - A subnet can be attached to one **Availability Zone (AZ)** and one **Route Table** only.
    - A **Route Table** can be associated with multiple subnets within the same VPC.
    #### Example:
        In a VPC with the following subnets:
        - `subnet-a` in `us-east-1a`
        - `subnet-b` in `us-east-1b`
        Both subnets can be associated with the **same Route Table** if they are part of the **same VPC**.

- **Difference Between Public & Private Subnets**:
    - **Public Subnet**: Its `Route Table` includes an entry that routes traffic to the public internet via an Internet Gateway (`IGW`).
    - **Private Subnet**: Its `Route Table` does not include an entry that routes traffic to an Internet Gateway (`IGW`).
---

# VPC Deep Dive