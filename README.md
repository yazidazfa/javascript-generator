# Odoo GDrive Connector Module Installation Guide

## Introduction

Welcome to the installation guide for our Odoo module. This module provides a choice to backup your odoo chatter attachment to your Google Drive. To ensure a smooth installation, follow the steps outlined below.

## Prerequisites

Before installing this module, make sure you have the following:

- Odoo installed and properly configured.
- Python and `pip` installed on your system.

## Installation Steps

1. **Download the Module**

   - Clone or download the module to your Odoo `addons` directory.

   ```bash
   git clone <repository-url> /path/to/your/odoo/addons
   ```

2. **Install Python Dependencies**

   - Navigate to the module's directory where the `requirements.txt` file is located.

   ```bash
   cd /path/to/your/odoo/addons/<module-name>
   ```

   - Use `pip` to install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. **Update the Odoo Modules List**

   - Restart your Odoo server to update the list of available modules:

   ```bash
   ./odoo-bin -c /path/to/your/odoo.conf -u all
   ```

4. **Activate the Module**
   - Log in to your Odoo instance.
   - Go to the **Apps** menu, search for your module, and click **Install**.


# How to Use Our Module

Follow these steps to set up and use our module to integrate with Google Drive.

## 1. Enable Google Drive API

- Go to [Google Cloud Console](https://console.cloud.google.com).
- Enable the **Google Drive API** and set up a **Service Account**.

## 2. Generate Service Account Key

- After creating the service account, click the three dots in the **Actions** column and select **Manage Keys**.
- Click **Add Key** and choose **Create New Key**.
- Select **JSON** as the key type, then click **Create**. The JSON file will be downloaded to your computer.

## 3. Upload Credentials in Odoo

- Open your Odoo application and go to the **Credentials** menu.
- Create a new record and fill in the fields to match the details in the downloaded JSON file.

## 4. Share Folder with Your Email

- Use the **Share Folder to Email** field to share the service account's folder with your email address. This will allow you to access the folder directly from your Google Drive.

## 5. Control File Visibility

- To make uploaded files **public**, check the **Is Public** checkbox.
- To keep files **private**, leave the checkbox unchecked.

## 6. Activate Your Google Drive Connection

- Use the **Is Active** checkbox to activate the record. Only **one record** can be active at a time for connecting to Google Drive.

## 7. Run the Initial Setup

- Go to **Scheduled Actions** in Odoo and manually run the **Montly Create Drive Folder** scheduled action for the first time. This will create the necessary folder in Google Drive.

## 8. Start Uploading Attachments

- Your chatter attachments will now be automatically uploaded to your Google Drive.




## Notes

- Ensure you have the necessary permissions to install Python dependencies on your system.
- If you encounter any issues, verify that all dependencies in `requirements.txt` are installed correctly.

## License

This module is distributed under the [appropriate license]. Refer to the LICENSE file for more details.

## Support

For any questions or assistance, please contact [support-email@example.com].
