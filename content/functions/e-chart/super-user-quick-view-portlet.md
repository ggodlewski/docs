---
title: "Super User Quick View Portlet"
date: "2020-03-10T16:24:00.920Z"
url: "functions/e-chart/super-user-quick-view-portlet.html"
version: 36
id: "1BmYr0t8bGa-s4VYN7njufXX2PC2W_aiVsKdqtijk9rI"
source: "https://drive.google.com/open?id=1BmYr0t8bGa-s4VYN7njufXX2PC2W_aiVsKdqtijk9rI"
menu:
    main:
        name: "Super User Quick View Portlet"
        identifier: "1BmYr0t8bGa-s4VYN7njufXX2PC2W_aiVsKdqtijk9rI"
        parent: "1DIVVSjNfv48-LekRsKDHFuHEm1gBYphsCC18iR2WikU"
        weight: 960
---
If you are a superuser and need access to view or edit the following areas of the [Control Panel](https://system/?f=layout&module=Admin&name=Home&tabmodule=admin&t=Admin) sidemenu, you will need additional security access to do so.

* [Layout Manager](https://system/?f=admin&subfunc=layout_manager&t=Layout+Manager&tabmodule=admin&tabselect=Layout+Manager)
* [Refer to Systems](https://system/?f=admin&subfunc=rts_editor&t=Refer+to+Systems&tabmodule=admin&tabselect=Refer+to+Systems) editor
* [System Report](https://system/?f=admin&s=system_report&tabmodule=admin&tabselect=System+Report) manager
* [System Settings](https://system/?f=admin&s=system_settings&tabmodule=admin&tabselect=System+Settings) editor
* [Esign Editor](https://system/?f=esign&s=dbe&tabmodule=esign&tabselect=Esign+Editor) ([E-Sign](https://system/?func=esign) sidemenu)
* [Tasklist Events](https://system/?f=tlist&s=tl_events&tabmodule=tasklist&tabselect=Tasklist+Events) ([Task List](https://system/?func=tlist) sidemenu)
* [System Configuration](https://system/?f=admin&s=sysconfigmgr&tabmodule=admin&tabselect=System+Configuration)
* Portions of the [Chart Tabs](https://system/?f=chart&s=cteditor&tabmodule=admin&tabselect=Chart+Tabs) editor

When trying to access any of the areas listed above and you do not have additional SuperUser access, an error message will display.



![](super-user-quick-view-portlet.images/image5.png)



{{% note %}}

Any SuperUser that requires a password to access those areas above should consult their MIE Implementer.

{{% /note %}}


To access and activate the SuperUser access required, the user must:

1. Add the<strong> SuperUser portlet</strong> to the [Quick View](https://system/) sidemenu.

![](super-user-quick-view-portlet.images/image1.png)

2. Next, locate the??Super User portlet and click the <strong>Unlock for this Session</strong> button.

![](super-user-quick-view-portlet.images/image4.png)

3. Enter the password provided by your MIE Implementer.

![](super-user-quick-view-portlet.images/image2.png)

4. Click the <strong>Enable</strong> button after keying in the password.
5. If successful, the button in the Super User portlet will display??<strong>Super user access enabled</strong>.??The super user can now go to those areas above, that were previously restricted.????

![](super-user-quick-view-portlet.images/image3.png)

6. If the system did not recognize the correct password, it will alert you to try again.



The password enables the logged-in superuser access to the areas mentioned above. In other words, after the superuser signs out, the superuser must re-enter the password into the portlet, in order to regain access to those areas. The password is not required for normal functionality.



