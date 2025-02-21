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

**Trigger_3: PopulateContactAddress**
- Scenario: Auto-Close Opportunity When Stage is "Closed Won"
- Use Case: If an Opportunity is marked as Closed Won, its Close Date should be updated to the current date.
- Triggering Object: Opportunity
- Event: Before Update
- Action: Set the Close Date when StageName changes to Closed Won.

**Trigger_4: PopulateContactAddress**
- Scenario: Send Email Notification When Case is Escalated
- Use Case: Whenever a Contact is created, it should inherit the Billing Address from the associated Account.
- Triggering Object: Case
- Event: After Update
- Action: Send an email to the Case owner when the IsEscalated field changes to true.
