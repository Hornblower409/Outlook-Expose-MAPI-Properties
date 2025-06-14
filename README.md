# Outlook-Expose-MAPI-Properties
 2025-06-01 - V1.1

    This is a modifed version of the original Code Two file from:
    https://www.codetwo.com/downloads/EXTENDED-PROPERTIES.CFG

    To install and use the MAPI Properties defined in this file see:
    https://www.slipstick.com/exchange/adding-extended-mapi-fields-to-outlook/

    Post any questions or comments on the SlipStick Outlook VBA and Custom Forms Forum at:
    https://forums.slipstick.com/forums/61-outlook-vba-and-custom-forms/

    Property Names and IDs from:
    https://msopenspecs.microsoft.com/files/MS-OXPROPS/%5BMS-OXPROPS%5D-090410.pdf

    File format of Form Configuration (.CFG) files from:
    https://learn.microsoft.com/en-us/office/client-developer/outlook/mapi/file-format-of-form-configuration-files

    ---------------------------------------------------------------------
    PR_LAST_VERB_EXECUTION_TIME           Time when the last verb was executed.

    PR_LAST_VERB_EXECUTED                 Last verb executed.

        Last_Verb_Reply_Sender = 102
        Last_Verb_Reply_All = 103
        Last_Verb_Reply_Forward = 104

    PR_SENT_REPRESENTING_EMAIL_ADDRESS    When sent by a Delegate, the email of the user who is represented by the Delegate.

    PR_INTERNET_MESSAGE_ID                Message ID field as specified in [RFC2822].

    PR_SENDER_EMAIL_ADDRESS               Message sender's email address.

    PR_CONTENT_FILTER_SCL                 Likelihood that the e-mail message is spam.

        See: https://learn.microsoft.com/en-us/openspecs/exchange_server_protocols/ms-oxcspam/2f279a5e-8daf-4b88-a833-7741d03f61f8

    PR_MESSAGE_FLAGS                      Bitmask of flags that indicate the origin and current state of a message.

        MSGFLAG_READ is a bit in the Message Flags that indicates if a message has been read.

        Unfortunatley, you can not expose this single bit setting as a MAPI property. The Microsoft docs
        incorrectly state that this Outlook Property (urn:schemas:httpmail:read) has a MAPI PropTag of
        "PidTagRead". This is not correct.


    PR_IN_REPLY_TO_ID                     The value of the original message's PR_INTERNET_MESSAGE_ID property value. 

    ---------------------------------------------------------------------
    To use the MAPI Properties defined in this file in a Rule:

        Step 1:
        [/] with selected properties of documents or forms
        Step 2:
        Click the underlined "selected properties"
        {In the Documents or Forms Properties Dialog}
        [Field \/]
        Forms ...
        {In the Select Forms Dialog}
        [Inbox \/]  
        Personal Forms
        Hornblower409 MAPI Props
        [Add]
        [Close]
        {Back in the Documents or Forms Properties Dialog}
        [Field \/]
        Hornblower409 MAPI Props  > {Pick a Prop}

    ---------------------------------------------------------------------
    To clear the Outlook Forms Cache

        Close Outlook
        Open a Windows Explorer to %LOCALAPPDATA%\Microsoft\FORMS
        Delete everything

 ---------------------------------------------------------------------
