---
aliases: []
cssclasses: []
tags: []
Related:
  - "[[/Agenda/Daily/2025-10-01 - Wednesday]]"
---
# Wednesday, October 01, 2025

[[/Notes/Yearly/2025|2025]] ❯ [[/Notes/Quarterly/2025 - Q4|Q4]] ❯ [[/Notes/Monthly/2025 - October|October]] ❯ [[/Notes/Weekly/2025 - Week 40|Week 40]]

❮ [[/Notes/Daily/2025-09-30 - Tuesday|Tuesday, September 30, 2025]] · Wednesday, October 01, 2025 · [[/Notes/Daily/2025-10-02 - Thursday|Thursday, October 02, 2025]] ❯

## 7:22

Okay, I've checked in with Vu

## 8:57

ClickUp has an API that we can interact with.

## 11:32

I'm thinking of what I can do for writing the release notes. I'm thinking I want to have a short description on what changed.

## 14:36

Okay, so I want to figure out how the fuck I can link to these different emails.

```vb
Sub CopyEmailLink()
    On Error GoTo ErrorHandler
    
    Dim mail As Outlook.MailItem
    Dim link As String
    
    ' Check if an email is selected
    If Application.ActiveExplorer.Selection.Count = 0 Then
        MsgBox "No email selected", vbExclamation
        Exit Sub
    End If
    
    ' Get the selected item
    Set mail = Application.ActiveExplorer.Selection.Item(1)
    
    ' Build the link (trim to remove any extra spaces)
    link = Trim("outlook:" & mail.EntryID)
    
    ' Copy to clipboard using Shell object
    With CreateObject("WScript.Shell")
        .Run "cmd /c echo|set /p=""" & link & """|clip", 0, True
    End With
    
    MsgBox "Link copied to clipboard!" & vbCrLf & vbCrLf & link, vbInformation
    
    Exit Sub
    
ErrorHandler:
    MsgBox "Error: " & Err.Description & vbCrLf & "Error Number: " & Err.Number, vbCritical
End Sub
```

```vb
Sub CopyEmailLinkForObsidian()
    On Error GoTo ErrorHandler
    
    Dim mail As outlook.MailItem
    Dim link As String
    Dim subject As String
    Dim markdownLink As String
    
    ' Check if an email is selected
    If Application.ActiveExplorer.Selection.Count = 0 Then
        MsgBox "No email selected", vbExclamation
        Exit Sub
    End If
    
    ' Get the selected item
    Set mail = Application.ActiveExplorer.Selection.Item(1)
    
    ' Get subject and build link
    subject = mail.subject
    link = Trim("outlook:" & mail.EntryID)
    
    ' Create Obsidian markdown link format
    markdownLink = "[" & subject & "](" & link & ")"
    
    ' Copy to clipboard
    With CreateObject("WScript.Shell")
        .Run "cmd /c echo|set /p=""" & markdownLink & """|clip", 0, True
    End With
    
    MsgBox "Obsidian link copied!" & vbCrLf & vbCrLf & markdownLink, vbInformation
    
    Exit Sub
    
ErrorHandler:
    MsgBox "Error: " & Err.Description & vbCrLf & "Error Number: " & Err.Number, vbCritical
End Sub
```

[Email](outlook:00000000BFD556235A0E444C89E441CA55935D350700E8E8888A3435F042A370079D2A1AF51C0000000001580000E8E8888A3435F042A370079D2A1AF51C0000116651F00000)

## 16:54

- Editing the subject line creates a "new email". It will show the email history in Outlook for the sender, but the receiver will not have any reference to this. The sender will be able to see the prior history, but will not be able to respond to it.
- You can "reply" to any portion of the email chain, but it'll simply be included at the end.
- Forwarding an email will show it in the email chain, but will not be visible to anyone other than the specified recipients.
- Copied emails will receive updates, but will not show an unread status.
- You can search for a category with: `category:"{category}"` where `{category}` is the category you're searching for. This does a partial match. You can also search for multiple categories at once like this: `category:"To Review" OR category:"To Document"`

