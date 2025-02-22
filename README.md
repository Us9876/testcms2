# testcms2
testcms2
# Article CMS (FlaskWebProject)


test
This project is a Python web application built using Flask. The user can log in and out and create/edit articles. An article consists of a title, author, and body of text stored in an Azure SQL Server along with an image that is stored in Azure Blob Storage. You will also implement OAuth2 with Sign in with Microsoft using the `msal` library, along with app logging.

## Log In Credentials for FlaskWebProject

- Username: admin
- Password: pass

Or, once the MS Login button is implemented, it will automatically log into the `admin` account.

## Project Instructions (For Student)

You are expected to do the following to complete this project:
1. Create a Resource Group in Azure.: testcms
2. Create an SQL Database in Azure that contains a user table, an article table, and data in each table (populated with the scripts provided in the SQL Scripts folder).: testcmsadmin / 123testcms@@@
    - Provide a screenshot of the populated tables as detailed further below.: testcms123  images container
3. Create a Storage Container in Azure for `images` to be stored in a container.Key: y0rSeNaepYgPNXIchEWp5XtBs1tM05MPkN70JZGPMWcUAT8XlKBqt3atVWaX05RTc4WiyZR86WWo+AStg+TbPg==
   connection string: DefaultEndpointsProtocol=https;AccountName=testcms123;AccountKey=y0rSeNaepYgPNXIchEWp5XtBs1tM05MPkN70JZGPMWcUAT8XlKBqt3atVWaX05RTc4WiyZR86WWo+AStg+TbPg==;EndpointSuffix=core.windows.net (not required)
    - Provide a screenshot of the storage endpoint URL as detailed further below.
        description secret: testcms
        value also   client can secret: 1RB8Q~6sV2M.vWy9Z3w86Wi4MQ5Vk~owJ99n7bgj
         be Also can secret key: scret id: 3d3a2ed3-8d00-429c-94ec-14e958a11434
         be application id: b15d75dd-2873-4e49-ad95-096d65bd0279
      
5. Add functionality to the Sign In With Microsoft button. : testcms
    - This will require completing TODOs in `views.py` with the `msal` library, along with appropriate registration in Azure Active Directory.
6. Choose to use either a VM or App Service to deploy the FlaskWebProject to Azure. Complete the analysis template in `WRITEUP.md` (or include in the README) to compare the two options, as well as detail your reasoning behind choosing one or the other. Once you have made your choice, go through with deployment.
7. Add logging for whether users successfully or unsuccessfully logged in.
    - This will require completing TODOs in `__init__.py`, as well as adding logging where desired in `views.py`.
8. To prove that the application in on Azure and working, go to the URL of your deployed app, log in using the credentials in this README, click the Create button, and create an article with the following data:
	- Title: "Hello World!"
	- Author: "Jane Doe"
	- Body: "My name is Jane Doe and this is my first article!"
	- Upload an image of your choice. Must be either a .png or .jpg.
   After saving, click back on the article you created and provide a screenshot proving that it was created successfully. Please also make sure the URL is present in the screenshot.
9. Log into the Azure Portal, go to your Resource Group, and provide a screenshot including all of the resources that were created to complete this project. (see sample screenshot in "example_images" folder)
10. Take a screenshot of the Redirect URIs entered for your registered app, related to the MS Login button.
11. Take a screenshot of your logs (can be from the Log stream in Azure) showing logging from an attempt to sign in with an invalid login, as well as a valid login.

## example_images Folder

This folder contains sample screenshots that students are required to submit in order to prove they completed various tasks throughout the project.

1. article-cms-solution.png is a screenshot from running the FlaskWebProject on Azure and prove that the student was able to create a new entry. The Title, Author, and Body fields must be populated to prove that the data is being retrieved from the Azure SQL Database while the image on the right proves that an image was uploaded and pulled from Azure Blob Storage.
2. azure-portal-resource-group.png is a screenshot from the Azure Portal showing all of the contents of the Resource Group the student needs to create. The resource group must (at least) contain the following:
	- Storage Account
	- SQL Server
	- SQL Database
	- Resources related to deploying the app
3. sql-storage-solution.png is a screenshot showing the created tables and one query of data from the initial scripts.
4. blob-solution.png is a screenshot showing an example of blob endpoints for where images are sent for storage.
5. uri-redirects-solution.png is a screenshot of the redirect URIs related to Microsoft authentication.
6. log-solution.png is a screenshot showing one potential form of logging with an "Invalid login attempt" and "admin logged in successfully", taken from the app's Log stream. You can customize your log messages as you see fit for these situations.

## Dependencies

1. A free Azure account
2. A GitHub account
3. Python 3.10
4. Visual Studio 2019 Community Edition (Free)
5. The latest Azure CLI (helpful; not required - all actions can be done in the portal)

All Python dependencies are stored in the requirements.txt file. To install them, using Visual Studio 2019 Community Edition:
1. In the Solution Explorer, expand "Python Environments"
2. Right-click on "Python 3.10 (64-bit) (global default)" and select "Install from requirements.txt"

## Troubleshooting

- Mac users may need to install `unixodbc` as well as related drivers as shown below:
    ```bash
    brew install unixodbc
    ```
- Check [here](https://docs.microsoft.com/en-us/sql/connect/odbc/linux-mac/install-microsoft-odbc-driver-sql-server-macos?view=sql-server-ver15) to add SQL Server drivers for Mac.
