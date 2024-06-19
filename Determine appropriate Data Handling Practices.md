
# Scenario

You work for an educational technology company that developed an application to help teachers automatically grade assignments. The application handles a wide range of data that it collects from academic institutions, instructors, parents, and students.

Your team was alerted to a data leak of internal business plans on social media. An investigation by the team discovered that an employee accidentally shared those confidential documents with an external business partner. An audit into the leak is underway to determine how similar incidents can be avoided.

A supervisor provided you with information regarding the leak. It appears that the principle of least privilege was not observed by employees at the company during a sales meeting. You have been asked to analyze the situation and find ways to prevent it from happening again.

First, you'll need to evaluate details about the incident. Then, you'll review the controls in place to prevent data leaks. Next, you'll identify ways to improve information privacy at the company. Finally, you'll justify why you think your recommendations will make data handling at the company more secure.

# Incident Summary

A sales manager shared access to a folder of internal-only documents with their
team during a meeting. The folder contained files associated with a new product that has not been
publicly announced. It also included customer analytics and promotional materials. After the meeting,
the manager did not revoke access to the internal folder, but warned the team to wait for approval
before sharing the promotional materials with others.

During a video call with a business partner, a member of the sales team forgot the warning from their
manager. The sales representative intended to share a link to the promotional materials so that the
business partner could circulate the materials to their customers. However, the sales representative
accidentally shared a link to the internal folder instead. Later, the business partner posted the link on
their company's social media page assuming that it was the promotional materials.

# Analysis

| Control| Least Privilege|
|---------|----------------|
|Issue(s)| The principle of least privilege was not maintained. Access to the shared folder was not redacted by the sales manager once the meeting ended.|
| Review| NIST SP 800-53: AC-6 addresses the issues found in this scenario. Specifically, the control enhacements of this framework outline the structure for automatically revoking escalated privileges after a pre determined duration. Regular audits should be performed as outlined in NIST SP 800-53: AC-6. However, this incident may have occurred entirely between audits and therefore the previous control is the most important step that was missed.|
|Recommendations| To improve the principal of least privilege, the sales manager could have presented the information from the confidential files on a projector screen and without sending them to employees that should not have access. In addition, activity logs of provisioned employees must be monitored should these files be shared in order to prevent them from being published incorrectly.|
|Justification| Sharing access to folders with sensitive information to employees that should not have access poses an unnecessary risk to the business. The sales manager must audit access to shared sensitive files if this action is necessary for business continuity.|


