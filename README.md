# basic-trigger-scenarios
This repository will be having basic trigger scenario which can we used in salesforce for business need

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

**Trigger_5: AssignLeadQueue**
- Scenario: Auto-Assign Lead to a Queue Based on Industry
- Use Case: A business wants to assign specific queue to lead whos Industry is Technology
- Triggering Object: Lead 
- Event: Before Insert
- Action: Assign leads to specific queues based on industry.

**Trigger_6: LogAccountFieldChanges**
- Scenario: Log Old and New Values on Field Change
- Use Case: A business wants to store the old value of field and new value of the field for tracking purpose.
- Triggering Object: Account 
- Event: after update
- Action: Store field history in a custom object.

**Trigger_7: RestrictCloseDateChange**
- Scenario: Prevent Opportunity Close Date Change After Stage Closed Won
- Use Case: A Business want to restric the user to change the close date when stagename is closed won.
- Triggering Object: Opportunity 
- Event: Before Update
- Action: Restrict CloseDate changes if StageName = Closed Won.

**Trigger_8: PreventTaskDeletion**
- Scenario: Prevent Task Deletion
- Use Case: A business want that no one delete the task record from any object
- Triggering Object: Task
- Event: before delete
- Action: Restrict task deletion.

**Trigger_9: SendSMSOnCaseClose**
- Scenario: Send SMS Notification When a Case is Closed
- Use Case: When a support case is resolved, the customer should receive a notification via SMS (or email) informing them that their case has been closed. This improves customer communication and service quality.
- Triggering Object:  Case
- Event: After Update
- Action: Send an SMS (or email) notification when a case is marked as "Closed."

**Trigger_10: UpdateContactStatusOnEmailBounce**
- Scenario: Update Contact Status When Email Bounces
- Use Case: If an email sent to a contact bounces, the contact's Status__c field should be updated to reflect that the email is invalid.
- Triggering Object: Contact
- Event: After Update 
- Action: Automatically update the Status__c field to "Email Bounced" when an email bounces.

**Trigger_11: PreventOpportunityDeletion**
- Scenario: Prevent Deleting Opportunity If There Are Related Quotes
- Use Case: Opportunities often have related Quotes. To maintain data integrity, users should not be allowed to delete an Opportunity if it has related Quotes.
- Triggering Object: Opportunity
- Event: Before Delete
- Action: Restrict Opportunity deletion if related Quotes exist.

**Trigger_12: AutoCreateOpportunityOnLeadConversion**
- Scenario: Auto-Create Opportunity When a Lead is Converted
- Use Case: When a Lead is converted, an Opportunity should be automatically created if one does not exist.
- Triggering Object: Lead 
- Event: After Update
- Action: Automatically create an Opportunity when a Lead is converted.

**Trigger_13: RestrictPrimaryContactChange**
- Scenario: Restrict Changing Primary Contact on Account If the Account is Active
- Use Case: An Active account should not allow its primary contact to be changed.
- Triggering Object: Account
- Event: Before Update
- Action: Prevent updates to the Primary Contact field when the account is active.

**Trigger_14: AssignCaseToQueue**
- Scenario: Auto-Assign Cases to Support Queues Based on Product
- Use Case: Cases should be assigned to the appropriate support queue based on the Product__c field
- Triggering Object: Case
- Event: Before Insert, Before Update
- Action: Automatically assign cases to the correct support queue

**Trigger_15: PreventStageChangeLowRevenue**
- Scenario: Prevent Opportunity Stage Change If Revenue < Expected
- Use Case: If the Revenue__c of an Opportunity is less than the Expected_Revenue__c, the stage should not be allowed to progress.
- Triggering Object: Opportunity
- Event: Before Update
- Action: Prevent stage change if revenue is below the expected amount.

**Trigger_16: SyncCustomFields**
- Scenario: Update Custom Fields When Related Records Change
- Use Case: If a related object (e.g., Account) is updated, a custom field in a child object (e.g., Contact) should be updated as well.
- Triggering Object: Account 
- Event: After Update
- Action: Sync custom fields between parent and child records.

**Trigger_17: CreateFollowUpTaskOnClose**
- Scenario: Auto-Create Task for Follow-Up After Opportunity Closure
- Use Case: When an Opportunity is closed (Won or Lost), a follow-up task should be created for the Account Owner.
- Triggering Object: Opportunity
- Event: After Update
- Action: Create a follow-up task after Opportunity closure

**Trigger_18: PreventUserDeactivation**
- Scenario: Prevent Deactivating Users Who Own Open Opportunities
- Use Case: A user should not be deactivated if they own open opportunities.
- Triggering Object: User  
- Event: Before Update
- Action: Restrict user deactivation if they have active opportunities

**Trigger_19: ContentVersion**
- Scenario: Prevent File Upload if Size Exceeds 10MB
- Use Case: Users should not be able to upload a file larger than 10MB to prevent excessive storage usage
- Triggering Object:  ContentVersion
- Event: Before Insert
- Action: Block files larger than 10MB and display an error message

**Trigger_20: DeleteAttachmentsOnParentDelete**
- Scenario: Auto-Delete Attachments If Parent Record Is Deleted
- Use Case: If a Case, Opportunity, or Account is deleted, all related attachments should also be deleted to free up storage space.
- Triggering Object: Case, Opportunity, Account
- Event: After Delete
- Action: Delete Attachments when the parent record is deleted

**Trigger_21: NotifyFileUploadToImportantRecord**
- Scenario: Notify Users When a File is Uploaded to an Important Record
- Use Case: When a file is uploaded to a high-value Opportunity (>$100K) or a Priority Case, notify the record owner via email
- Triggering Object:  ContentDocumentLink
- Event: After Insert
- Action: Send an email notification when a file is uploaded to a high-priority record


