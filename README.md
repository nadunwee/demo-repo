# Google Drive Uploder
    
## Description:
This Python program uploads files or folders to Google Drive using the Google Drive API v3. It requires the Google API client library to be installed, which provides the necessary modules for accessing the Drive API.

The program takes command line arguments to determine whether a single file or an entire folder is being uploaded. It then authenticates the user's Google account using OAuth 2.0, which involves creating or using an existing credentials file (token.json) to store the user's access and refresh tokens. The credentials file is automatically created when the user first authorizes the program, and it is used in subsequent runs of the program to authenticate the user without requiring further authorization.

Once authenticated, the program creates a MediaFileUpload object for the file or folder to be uploaded. This object specifies the MIME type of the file (in this case, image/jpg for JPEG images), and is used to upload the file to Google Drive in chunks to avoid running out of memory. The program also creates a file resource with metadata, which includes the name of the file or folder and the ID of the parent folder in Google Drive where it will be uploaded.

The program then sends a request to upload the file or folder using the files().create() method of the Drive API, passing in the file resource and MediaFileUpload object as arguments. If the upload is successful, the program prints a message to the console confirming that the file or folder has been uploaded and providing the unique ID assigned to it by Google Drive.

If an error occurs during the upload, the program catches the HttpError exception and prints an error message to the console.

Overall, this Python program provides a simple and convenient way to upload files or folders to Google Drive from the command line, which can be useful for automating routine file backup tasks or integrating with other scripts and programs.
