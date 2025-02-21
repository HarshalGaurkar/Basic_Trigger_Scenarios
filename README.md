**Below Are the details description of the trigger with there name and usecase**

**Trigger_1: PreventDuplicateAccounts**
- Scenario: Prevent Duplicate Account Creation
- Use Case: A business wants to prevent users from creating duplicate Account records with the same Name.
- Triggering Object: Account
- Event: Before Insert
- Action: Check for existing accounts with the same name and prevent insertion if found.

**Trigger_2: PopulateContactAddress**
- Scenario: Auto-Populate Contact Field Based on Account
- Use Case: Whenever a Contact is created, it should inherit the Billing Address from the associated Account.
- Triggering Object: Contact
- Event: Before Insert, Before Update
- Action: Fetch and populate the Mailing Address from the related Account.
