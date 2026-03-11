# HRM Integration (Finch)

This article explains how to integrate your HRM (Human Resource Management) system with Light using Finch — including what data is synced, what information we need from you, and how the activation process works.

[Open in Light →](https://app.light.inc/settings/integrations)

## How Light connects to HRM systems

Light connects to HRM systems through **Finch**, a secure third-party connector that supports over **200+ HRM providers** globally.

You or your Customer Success Manager (CSM) can check provider compatibility here: [Finch Integrations](https://www.tryfinch.com/integrations)

## Data synced into Light

Light imports key **organisational employee data** from your HRM, including:

- Name
- Email
- Manager
- Active / inactive status
- Entity (based on selected field)
- Department (if applicable)

**Note:** Payroll data is **not** synced.

## Sync frequency

Sync frequency depends on your HRM provider.

Light will automatically pull employee data:

- **Daily** (every 24 hours), or
- **Weekly** (every 7 days)

## User behavior in Light

When the HRM sync runs:

- **New employees** are automatically added to the **Users** list in Light
- **Removed employees** are automatically deactivated or removed
- A **default base role** is automatically assigned to all new users created via HRM sync

## Integration steps

### Step 1 — Customer connects HRM in Light

Go to **Settings (gear icon) → Integrations → Add Integration → HRM**

1. Log in using your **HRM admin credentials**

### Step 2 — Internal configuration in Finch

After the HRM connection is established, Light configures data mapping in **Finch** using **three key inputs** provided by the customer (see below).

This setup is performed **internally by Light** — customers do not configure this step.

### Step 3 — First sync

Once the mapping is complete, the first sync will automatically pull employees into Light.

They will appear under **Users** after the next scheduled sync.

## Information required from the customer

1. **Default Base Role**
   - What role should be assigned to all synced employees by default?
   - Example: "Reimbursement Only"

2. **Entity / Company Mapping Field**
   - Which HRM field should Light use to identify the employee's **Entity**?
   - Examples: "Country of Employment", "Legal Entity", "Location"
   - Please provide the **exact field name**

3. **Departments / Groups**
   - Should Light import department or group information?
   - If yes, specify which HRM field represents this
   - Examples: "Department", "Team", "Business Unit"

## Key points

- Light connects to HRM systems via **Finch**
- Employees are **auto-created and removed** in Light based on HRM data
- **Three customer inputs** are required per integration
- **Payroll data** is not included in the sync

## Related articles

- [Integrations overview](11-1-integrations-overview.md)
- [User roles and permissions](../03-user-management/03-2-roles-permissions.md)
