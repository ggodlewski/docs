---
title: "Refill All"
date: 2020-03-16T11:56:29.091Z
url: "refill-all.md"
author: Jeremia Ploor
id: 10JqzKZ8UPQ0gfq0wqBGWqbHNwEgUyLtsFVGjpG5shYA
source: https://drive.google.com/open?id=10JqzKZ8UPQ0gfq0wqBGWqbHNwEgUyLtsFVGjpG5shYA
menu:
    main:
        name: "Refill All"
        identifier: "10JqzKZ8UPQ0gfq0wqBGWqbHNwEgUyLtsFVGjpG5shYA"
        parent: "1BT9iwpUSk65PGOkXhOqxTjwNvG-JzY6aKqNw1elTkKA"
        weight: 2120
---
Refill All Quick Link

Make sure system setting *Use Fill Requests* is set to zero if you wish to use the Refill All feature (unless using Inventory module)

![](external_files/2de50bc8e33daec505a76a3cb3a9360e.png)

The Refill All link is a quick link to display all medications in a list format and you can click check-mark boxes to refill multiple prescriptions at a time, instead of going into each prescription individually to refill.

![](external_files/c2c5675ebb6346ceb6dc21e739f8beb6.png)

When you click on this, it opens the **Refill Meds** screen.

Here is a listing of all the patient's prescriptions. It will automatically have a check-mark in the box to the left of the drug name **if** this prescription/drug needs a refill because the refills are ‘due' according to the quantity, date prescribed and # of refills that have been used according to the calculated initial prescribe date. You can still refill a prescription even if the criteria above isn't met according to the system.

**Your MIE Implementer can have your system set to 3 different options in the Refill module to provide further security for refill requests:**

![](external_files/522a61bc16473ef39b9d84647478b012.png)

* <strong>System setting 0</strong> means that your system will not task the provider but the office staff will be able to print/fax a refill without waiting on the provider. (This is what every system is defaulted to unless changed.)
* <strong>System setting 1</strong> means all refill requests for your system will task the provider for approval first. The refill request requires the prescribing physician to approve any refills (via automatic task) before they can be printed or faxed.
    * After the prescribing physician approves (via task) then the refills can be printed/faxed after approving. Your implementer can turn on these system settings to allow that security feature for just the prescribing physician of the original prescription to approve any refills in this module.
* <strong>System setting 2</strong> means your system will display the option to either task the provider for approval or office staff can print/fax the refill.

More system settings that your MIE Implementer will need to set depending on your refill setting:

![](external_files/a808fa904acf4d0b2364951792735ae5.png)

The next pages will describe these different system options.

## System Setting is Zero

If your system setting is set to 0 it means that your system will not task the provider but the office staff will be able to print/fax a refill without waiting on approval from the provider or tasking the provider.

![](external_files/522a61bc16473ef39b9d84647478b012.png)

The REFILL ALL screen will look like below.

![](external_files/da20f55cdad4d7685d8717208621cab0.png)

The fields at the top are there to help you set duration, refills & prescriber in ‘mass' which will automatically set the below listed medications needing refilled to that specific information. This does it in mass and quickly instead of individually.

![](external_files/261e4e4dd7bc3de5b87469b618b09c6d.png)

* <strong>Refill Date:</strong> Type/select the date you are refilling the meds.
* <strong>Check All</strong> box: You can select <em>Check All</em> to select <strong>all</strong> the drugs in the listing to be refilled. Or you can individually check-mark the box next to the <em>Drug Name</em> to select the specific drug(s) to be refilled.
    * The <em>Check-All </em>option then changes to <em>Uncheck All</em>. You can click Uncheck All if you want to start over and clear the check-mark boxes in drug name selection.
    * Whatever medications you want to have refilled <strong>must </strong>have a check-mark on them. The ones without check-marks will not be refilled.

![](external_files/da20f55cdad4d7685d8717208621cab0.png)

* <strong>Print All Drug Guides</strong> box: Click this to check-mark all the prescriptions/drugs in the listing to <em>print</em>. If you click <em>Print All</em> then it will set checks on all the drugs in the <em>Print Drug Guide</em> column on the far right side of each drug name. The <em>Print All</em> option then changes to <em>Unprint All</em>. You can click <em>Unprint All</em> if you want to start over and clear the print check-mark boxes. You can also individually un-checkmark which drug you don't want to print a Drug Guide for.

![](external_files/da20f55cdad4d7685d8717208621cab0.png)

* <strong>Print All Prescriptions</strong> box: If your system is set up that the physician has to approve any refills, this button will not show for you (see next pages of explanation). If you are allowed to refill prescriptions automatically, click this to check-mark all the prescriptions/drugs in the listing to <em>print</em>. If you click <em>Print All</em> then it will set checks on all the drugs in the <em>Print Script</em> column on the far right side of each drug name. The <em>Print All</em> option then changes to <em>Unprint All</em>. You can click <em>Unprint All</em> if you want to start over and clear the print check-mark boxes. You can also individually un-checkmark which drug you don't want to print a Script for.
* <strong>Duration & Refills & Prescriber</strong>: Whatever you type in this field and click <em>SET</em> beside each, then it will apply that information to <strong>all</strong> medications/drugs in this refill listing. These are settings that can be quickly applied for the whole entire list which would make it quicker if you wanted to assign the same prescriber, etc to all of the meds that you are refilling. These fields will only be <strong>applied</strong> if you have a drug/prescription check-marked for refilling. It will <strong>show</strong> all the meds on the list as changed duration/refills/and/or prescriber that you <em>set</em> it for— but it will only actually change/apply those to the check-marked drugs you are refilling when you click <em>SUBMIT</em>.

![](external_files/da20f55cdad4d7685d8717208621cab0.png)

* You <strong>must</strong> select a prescriber for all refills. If you do not, you will see an error message that you need to select a prescriber.
* When you go back into MEDS TAB you will see your original settings on any drugs that you did <strong>not</strong> check-mark to refill, meaning, the "<em>sets"</em> that you did only affect the check-marked refill prescriptions you want. You can, of course, go through and individually set the Duration, Refills, Prescriber also for an individual drug name in the refill list instead of setting in mass quickly.
* <strong>Drug Name:</strong> Make sure you have check-marked which drug names you wish to refill (or use the CHECK ALL button above this section). This Drug Name section currently sorts by two criteria. It first sorts by the end date (if one is specified) and then alphabetically.  So things that will at some point be due for a refill (have an end date) are at the top—because those are the ones that need attention to be refilled first and not get missed.  And things that don't look like they are going to be refilled (no end date) are at the bottom.  Inside those two groups, the drug names should be alphabetical.

![](external_files/da20f55cdad4d7685d8717208621cab0.png)

* <strong>Comments:</strong> Any previous comments tied to the drug will appear. You can add/edit comments from the field in each individual drug name also. These comments showing here in the refill all screen can be turned on or off for the entire system. If turned off, the entire comments line will not show here for each med listed in the refill all screen. If turned on, you will always see the comments line for each med in the refill all page. Contact your MIE representative for this change in the system settings.
* <strong>Note to Pharmacist:</strong> Any previous notes to the pharmacist will appear. You can add/edit notes to the pharmacist here also.

![](external_files/0a3c790811b8f1e00f0052e788a52d88.png)

* <strong>Drug Guide:</strong> Checkmark this if you want the drug guide for this med to be placed in the print/fax queue.

![](external_files/9f36852145ddd10fb1a382439f7f457a.png)

* <strong>Print Script:</strong> Will be checkmarked to put this refill in the print/fax queue. This check-box will not show up if your practice is set to have the prescribing physician approve all refills first. The physician would approve it in his tasks, then that med refill would then be placed in the patient's print/fax queue.

Click *SUBMIT* at the top or bottom of the screen when you have selected all the prescriptions you wish to refill, have changed/updated all the information/fields and checked whether to print or not.

Upon submission, your screen will refresh and be back at the Meds tab. It will display in the print/fax queue any refilled prescriptions you submitted and also any drug guides to print (if you so selected).

![](external_files/d33eda63a3f7c857d4a094f07fabf5e3.png)

## System Setting is One

If your system setting is set to 1 it means all refill requests for your system will task the provider for approval first. The refill request requires the prescribing physician to approve any refills (via automatic task) before they can be printed or faxed. After the prescribing physician approves (via task) then the refills can be printed/faxed after approving. Your implementer can turn on this system setting to allow that security feature that requires the prescribing physician of the original prescription to approve any refills prior to printing/faxing them.

![](external_files/ccad534113c2a5f161e77a11ec362285.png)

If your system has been requested to be set up this way, when you are in Refill All you will see a message at the top stating that after you submit the refill request, it must be approved by the prescribing physician first. There is no way for you to print/fax this refill until the physician approves it.

![](external_files/419f13107a23789dcd6ee7b50677b50b.png)

Users will not see a check-box option for *Print Script*. The system tasks the physician for a refill approval first. A message is shown "Prescribing physician must approve refills before they can be printed or transmitted."

Fill out the refill fields to request the refill, make sure the medication to refill is check-marked. Whatever medications you want to have refilled **must** have a check-mark on them. The ones without check-marks will not be refilled. Then click SUBMIT.

After you click SUBMIT for the refill request, this will send a task to each prescribing physician for each & every medication that was check-marked as requested to be refilled along with the details in the fields you filled out (duration, quantity, etc). This will put the refill into a pending status, meaning that it will not be displayed in the patient's queue of scripts or drug guides to print. The prescribing physician of the medication will be sent a task called *Refill Approval.*

![](external_files/4460f618bd1278d6a429803a5c96cf8c.png)
The prescribing physician receives the task and **must click Perform** to perform a refill authorization for the Refill Approval task. It will take the prescriber to either the single refill page or the refill all page for that patient.

There, the prescriber can see the patient allergies, list of current meds, and conditions, etc.  The prescriber then can enter any additional notes.  Once he/she clicks on the PRESCRIBE REFILL button, the prescribing physician's task will be completed and the medication is set to be refilled in the patient's account.

![](external_files/11add02e89ff732ff3d2296ab9df8022.png)

The medication will appear in the patient's e-meds module as pending to print/fax in the queue. It is then the prescriber's responsibility to print/fax the refill or notify someone to do so (unless an automatic reply task is turned on for your practice).

An approved refill request for controlled substances now send a "Denied - New Prescription to Follow" message, and set the new refill/script in {{% system-name %}} to a "needs printed" status.

**Automatic reply task:** MIE can turn on a setting in your system to have a reply task instantly sent back to the requesting user's department that originally requested the Refill Approval for the medication. If this setting is turned on for your system, a task will be sent back to that entire department saying the prescriber has completed their task, approved the refill & can now be printed/faxed. Anyone within that department would be notified of this & can then complete the print/fax of the approved medication refill.

![](external_files/62f59b572a118112fd38ec1f97ab2c5d.png)

## System Setting is Two

If your system setting is set to 2 it means your system will not mandate the staff to task the provider for refill approval, but does give the staff this option. However, the office staff still is able to print/fax a refill that is not checkmarked to task the provider.

![](external_files/4065745bf00954d761d540290bbe1738.png)

The REFILL ALL screen will look like the below. At the top, it will have the *Task Prescriber for Approval* check-marked as a default. Having this check-marked to task for approval will task the provider for the refill approval for all the drugs below it with a check-mark in the drug name column. Whatever medications you want to have refilled **must** have a check-mark on them. The ones without check-marks will not be refilled.

![](external_files/0f60492b7f6d9047850afce85305696a.png)

Any drug names to refill that are check-marked will be tasked to the prescriber for refill approval upon submission. The user has to wait for approval then before printing/faxing the refill.

The user also though can _un_check-mark the Task Prescriber for Approval box and check off drug names to refill in this module and submit. Whatever medications you want to have refilled **must** have a check-mark on them. The ones without check-marks will not be refilled.

This will *not* task the prescriber for these refills and they will render in the print/fax queue without provider approval.

![](external_files/2b21fea1a7ec426e892d367123c25879.png)

Any medication refill pending prescriber approval will also display as a message *(pending approval)* in the patient's medication history in the comments column.

![](external_files/c6d71efb068e691a18e1edec258f07a7.png)
