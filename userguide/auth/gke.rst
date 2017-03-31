=============================
Google Container Engine (GKE)
=============================

**Create a New Project**

StackPointCloud must be set up to manage a project within your Google Container Engine (GKE) account. To do this, log into the Google cloud console at https://console.cloud.google.com.

Click **Project** to open the drop-down menu.

.. image:: ../img/gke-1-click-project.png

Click **Create Project** on the drop-down menu.

.. image:: ../img/gke-2-create-project.png

Fill in "StackPointCloud" as the project name, then click **Create**.

.. image:: ../img/gke-3-name-and-create.png

It may take a few moments for the project to be created. Once the task is complete, you will be redirected to the project Dashboard.

.. image:: ../img/gke-4-dashboard.png

The next step is to use the API Manager to enable the Google Container Engine API for this project. To do this, scroll down and click **Use Google APIs**.

.. image:: ../img/gke-5-use-google-api.png

This will take you to the API Manager Dashboard. Click **ENABLE API**.

.. image:: ../img/gke-6-enable-api.png

This will take you to the API Library. Click **Container Engine API**.

.. image:: ../img/gke-7-click-container-engine-api.png

This will take you to the Container Engine API page. Click **ENABLE** to enable the API.

.. image:: ../img/gke-8-enable-container-engine-api.png

**Create Credentials**

After the new project has been created, Google will prompt you to create credentials by clicking the **Go to Credentials** button.

.. image:: ../img/gke-9-go-to-credentials.png

Click the link to skip this step and go directly to **service account**.

.. image:: ../img/gke-10-service-account.png

On the Service Accounts page, click **CREATE SERVICE ACCOUNT** to create a new service account.

.. image:: ../img/gke-11-click-create-service-account.png

In the **Service Account Name** field, give your account a name like `spc-admin`. For **Role** select **Project** > **Owner**.

.. image:: ../img/gke-12-service-account-name-and-roles.png

Tick the box to **Furnish a new private key** and select **Key type:** **JSON** then click **Create**.

.. image:: ../img/gke-13-click-create-service-account.png

You will be prompted to save the JSON credentials (keyset) to your local computer. Copy and paste these into 'the StackPointCloud website <http://stackpoint.io>'_ when you create a new cluster.
