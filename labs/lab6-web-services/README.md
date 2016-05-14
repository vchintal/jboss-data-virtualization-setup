## Web Services Generation

|Quick Index|
|:---------|
|[RESTful Web Services](#restful-web-services)|
|[Internal Materialization](#internal-materialization)|
|[External Materialization](#external-materialization)|

---

### RESTful Web Services 

The easiest approach to generating Web Services is to let the Teiid Designer generate those for you. To generate the **REST** service for a view table, we need to have in place a virtual stored procedure that takes as many input parameters as the number of columns that constitute the primary key of the view table. Cases when there is no primary key on the view, then there are no input parameters to the virtual stored procedure.

#### Generate the REST war

**Step 1:** Right-click on the **Customers** view model and select **Modeling → Generate REST Virtual Procedures**, as shown in the image below:

[![](.images/ws-create-rest-procedures.png)](.images/ws-create-rest-procedures.png)

**Step 2:** Fill in the details as shown in the image below and click on **OK**

[![](.images/ws-create-rest-procedures-conf.png)](.images/ws-create-rest-procedures-conf.png)

**Step 3:** Save the **Customers** view model, click **Synchronize All** in the **dvdemo.vdb** and the right-click on the VDB and select **Modeling → Generate REST war** as shown below:

[![](.images/ws-generate-rest-war.png)](.images/ws-generate-rest-war.png)

**Step 4:** Fill in the details in the pop-up window as shown below. Choose the folder of your choice for saving the WAR file. In this example the file is saved in the **lab6-web-services** folder.

[![](.images/ws-generate-rest-war-conf.png)](.images/ws-generate-rest-war-conf.png)

**Step 5:** Deploy the VDB first (right-click on the VDB → Modeling → Deploy) before you attempt to deploy the generated **REST** war file in the manner shown below.

[![](.images/ws-deploy-rest-war.png)](.images/ws-deploy-rest-war.png)

#### Test the REST war

Access the URL [http://127.0.0.1:8080/dvdemo/](http://127.0.0.1:8080/dvdemo/#!/Customers/all_customersRestProc) to access the deployed **REST** war and use the two REST methods as shown in the images below

[![](.images/ws-rest-test1.png)](.images/ws-rest-test1.png)

[![](.images/ws-rest-test2.png)](.images/ws-rest-test2.png)
