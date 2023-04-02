# Google Drive Uploder
    #### Video Demo:  <URL HERE>
    #### Description:
    This Python program uploads files or folders to Google Drive using the Google Drive API. The program imports required libraries, including the Google
    authentication library, and defines necessary scopes and arguments. The main function of the program checks the command-line arguments and uploads the
    specified file or folder to the Google Drive folder with the given folder ID.

    The program authenticates the user using the Google OAuth 2.0 authentication protocol, retrieves or creates the token.json file for authorization, and then
    creates an instance of the Google Drive API using the build function.

    For file upload, the program creates a MediaFileUpload object for the specified file, sets metadata with a name and a folder ID, and then sends a request to
    upload the file using the create method of the files resource. For folder upload, the program iterates over all files in the specified folder, creates a
    MediaFileUpload object for each file, sets metadata with a name and a folder ID, and then sends a request to upload the file.

    If an error occurs during the file or folder upload, the program catches the HttpError and prints the error message. Otherwise, the program prints a success
    message with the name and ID of the uploaded file or folder.

    Let me know if there are any further questions, comments, or concerns about this final.

    This is CS50P!
