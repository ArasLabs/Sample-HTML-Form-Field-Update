# Refresh Form Field on Load Sample

Some forms contain HTML fields that do not refresh on actions like save. That is because these fields reference Item properties, and do not actually point to them.

To refresh these properties you can use an onFormPopulate event containing method code to repopulate the field. 
This same type of mechanism can be used for other aspects of the Item window, but this sample just covers the Status field on the Project Template form. 

## Project Details

See [TESTSTATUS file](./TESTSTATUS.md) for latest testing information.

#### Built Using:
Aras 11.0 SP9

#### Versions Tested:
Aras 11.0 SP7, Aras 11.0 SP9

#### Browsers Tested:
Internet Explorer 11, Firefox 38 ESR, Chrome

> Though built and tested using Aras 11.0 SP9, this project should function in older releases of Aras 11.0.

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. htmlFormFieldUpdate import package

### Install Steps

1. Backup your code tree and store the backup in a safe place.
2. Copy the Innovator folder from the project's CodeTree subdirectory.
3. Paste the Innovator folder into the root directory of your Aras installation.
  * Tip: This is the same directory that contains the InnovatorServerConfig.xml file.
4. Backup your database and store the BAK file in a safe place.
5. Open up the Aras Package Import tool.
6. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
7. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
8. Enter the path to your local `..\CustomFormCSS\Import\imports.mf` file in the Manifest File field.
9. Select **CustomFormCSS** in the Available for Import field.
10. Select Type = **Merge** and Mode = **Thorough Mode**.
11. Click **Import** in the top left corner.
12. Close the Aras Package Import tool.

## Usage

1. Log in to Aras as admin.
2. Click **Templates > Project Templates** in the table of contents (TOC).
3. Open an existing Template, or create a new Template to view the status field on the Project Template form. Upon save it should look something like this:

![HTML Form Field Update](./Screenshots/htmlFormFieldUpdate.PNG)

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Original code written by Aras Corporation Support for Aras Corporation.

Updated and Documented by Jillian Jakubowicz for Aras Labs. @JillJakubowicz

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
