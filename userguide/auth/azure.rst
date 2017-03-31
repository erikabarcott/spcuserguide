======
Azure
======

In order to access Azure resources, the account must be authorized against the Azure Active Directory. For more information on creating a user account, see `the official Microsoft article <https://azure.microsoft.com/en-us/documentation/articles/active-directory-create-users/>`_).

To create a user account, first log into the Azure classic portal at https://manage.windowsazure.com with the credentials of the account owner.

Click **Active Directory** on the left-hand side of the screen. (Scroll down if necessary.)

.. image:: ../img/azure-auth-1-active-directory.png

Click **Default Directory**.

.. image:: ../img/azure-auth-2-default-directory.png

Click the **Users** tab.

.. image:: ../img/azure-auth-3-users.png

Click **Add User**, which is located at the very bottom of the browser window.

.. image:: ../img/azure-auth-4-add-user.png

Choose the user type from the drop-down menu, fill out the user name, then click the arrow in the lower right-hand corner to continue.

.. image:: ../img/azure-auth-5-user-info.png

On the next tab, fill out the user's first and last name and display name. For **Role** select "User." Click the arrow in the lower right-hand corner to continue.

.. image:: ../img/azure-auth-6-user-profile.png

Click the green **Create** button to create the account and get a temporary password for the user. Save this password.

.. image:: ../img/azure-auth-7-click-create.png

In a different browser, or in an incognito browser tab, go to the `Azure classic portal <https://manage.windowsazure.com>`_ and log in with the user that you just created.

You will be prompted to update the password. Fill out the current (temporary) password, then the new password twice. Click **Update password and sign in** to  set the new password and continue.

.. image:: ../img/azure-auth-8-update-password.png

The next step is to give the user account access to the subscription.
Log in to https://portal.azure.com with the subscription owner account and click **Subscriptions** on the left-hand side of the screen.

.. image:: ../img/azure-auth-9-subscriptions.png

Click the subscription you want to use for this user.

.. image:: ../img/azure-auth-10-select-subscription.png

Click the "little people" icon on the right-hand side of the screen.

.. image:: ../img/azure-auth-11-little-people.png

Click **Subscription admins**.

.. image:: ../img/azure-auth-12-subscription-admins.png

Click **Assigned To**.

.. image:: ../img/azure-auth-13-assigned-to.png

Click **Manage**.

.. image:: ../img/azure-auth-14-manage.png

This will take you to the Azure Classic portal. Here, you can enter the user as a co-administrator.

To do this, click **Add**, which is located at the very bottom of the browser window.

.. image:: ../img/azure-auth-15-add.png

Fill out the user's email address, tick the box to select the plan, then click the arrow which will appear in the lower right-hand corner.

.. image:: ../img/azure-auth-16-add-coadmin.png

This process will create the following three tokens, which you can use for access:

* `AZURE_SUBSCRIPTION_ID`: A 32-character hexadecimal dash-separated string.
* `AZURE_USERNAME`: The email account name, xxxx@domain.com
* `AZURE_PASSWORD`: The new (permanent) password.
