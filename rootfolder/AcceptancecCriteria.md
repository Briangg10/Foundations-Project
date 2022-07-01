### Brian Gonzalez
### Bug Catcher Acceptance Criteria

Manager Acceptance Criteria

FEATURE: Managers should be able to login to access their homepages
SCENARIO: As a manager I want to sign in so I can view my custom homepages

GIVEN: The manager is on the login page
WHEN    The managers enter his username
WHEN    the manager enter is password
WHEN    the manager clicks the login button
THEN    the manager should be logged in to the manager home page

FEATURE: Managers should be able to create defects
SCENARIO: As a manager I want to create defects so that I can start addressing them

GIVEN: The manager is on the manager page
WHEN    The manager enters defect into defect text box
WHEN    The manager enters a description of the defect
WHEN    The manager enters status of the defect
WHEN    The manager clicks on the create defect button
THEN    The manager should of created a defect


FEATURE: Managers should be able to assign defects
SCENARIO: As a manager I want to assign defects so that the defects can be worked on

GIVEN: The manager is on the manager page
WHEN: The manager should be able to view current defects and the defects status in defects table(waiting to be assigned, pending verification, accepted, declined, shelved,pending, etc)
WHEN: The manager in the defects tables views the defects thats needs to be assigned 
WHEN: The manager is able to assigned a defect to a tester in a columnn in the defect table by a drop down menu.
WHEN: The manager clicks on the assign button
THEN: The manager should had assigned a defect to a tester.


TESTER ACCEPTANCE Criteria

FEATURE: Testers should be able to login to access their homepages
SCENARIO: As a tester I want to sign in so I can view my custom homepage

GIVEN: The Tester is on the login page
WHEN    The Tester enter his username
WHEN    the Tester enter is password
WHEN    the Tester clicks the login button
THEN    the Tester should be logged in to the tester home page

FEATURE: Testers should be able to to view defects addressed to them.
SCENARIO: As a tester I want to view defects addressed to them so that they can begin working on the defects.

GIVEN   The tester is on the tester page
WHEN    The tester clicks on view defects button
WHEN    The tester is displayed a table showing them defects assgined to them
THEN    The tester should then be able to view the defecst assigned to them.

FEATURE: Testers should be able to update defects so they can monitor their progress
SCENARIO: As a tester I want to update defects so that they can monitor defect progress.
WHEN: Testers should be able select via drop down menu in the defects table if they want to accept or decline
WHEN: The Testers select accepted another column should appear
WHEN: The Tester is done updating their defect they should be able to select if the defect was fixed, rejected, or shelved in this column
THEN: The manager defect able on the manager page should be updated with the update status of the defect

Scenario: Update from pending to accepted
GIVEN:  The Tester has viewed their assgined defect
WHEN:   The tester clicks on accept on the defect column
WHEN:   The defect status is updated on manager page as accepted: work in progress

Scenario: Update from accepted to fixed
GIVEN:  The Tester has accepted their assgined defect
WHEN:   The tester clicks on accept on the defect column
WHEN:   The tester fixes the defect
WHEN:   The tester selects that the defects has been fixed
THEN:   The managers page is updated that the defect has been fixed

Scenario: Update from accepted to refecjed
GIVEN:  The Tester has accepted their assgined defect
WHEN:   The tester clicks on accept on the defect column
WHEN:   The tester can't fix the problem
WHEN:   The tester selects that the defects has been rejected: Invalid Bug. This means the defect can't be fixed at all.
THEN:   The managers page is updated that the defect has been rejected: Invalid Bug

Scenario: Update from accepted to shelved
GIVEN:  The Tester has accepted their assgined defect
WHEN:   The tester clicks on accept on the defect column
WHEN:   The tester can't fix the defect but another tester could be able to
WHEN:   The tester selects that the defects has been shelved. Shleved means it is put on standby.
THEN:   The managers page is updated that the defect has been Shelved: Unable to fix


Scenario: Update from pending to rejected
GIVEN: The tester has viewed thier assigned defect
WHEN: The tester clicks on decline on the defect column
WHEN: The defect status is updated on the manager page as declined
WHEN    The defect status show Decline: LOW PRIORITY


