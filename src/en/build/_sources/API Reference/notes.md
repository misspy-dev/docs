# `misspy.Bot.notes`
## notes
Get a list of notes.

| Name | Type | Default | Description |
| - | - | - | - |
| local | bool | False | Get only locally created notes. <br> |
| reply | bool | | If set to `True`, only replies will be retrieved; if set to `False`, all other than replies will be retrieved. If you do not set a value, you will get the note regardless of whether it is a reply or not. <br> |
| renote | bool | | If set to `True`, only renotes will be retrieved; if set to `False`, all other than renotes will be retrieved. If you do not set a value, you will get the note regardless of whether it is a renote or not. |
| withFiles | bool | | If set to `True`, only notes with attachments will be retrieved; if set to `False`, only notes without attachments will be retrieved. If no value is set, the note will be retrieved with or without attachments. |
| poll | bool | | If set to `True`, only notes with votes will be retrieved, if set to `False`, only notes without votes will be retrieved. If you do not set a value, you will get the note regardless of whether it has a vote or not. |
| limit | int | 10 | Specifies the maximum number of notes to retrieve. |
| sinceId | str | | If specified, returns notes whose id is greater than that value. <br> |
| untilId | str | | If specified, returns notes whose id is less than that value. <br> |

## notes_create
Create a note. Reply and Renote are also done with this function.

| Name | Type | Default | Description |
| - | - | - | - |
| visibility | str<br>(`public` `home` `followers` `specified`) | public | Publicity of the note. |
| visibleUserIds | list<br>(str) | | List of IDs of users who can view the note. Applies only when visibility is specified. <br> |
| text | str &#124; None | | The text of the note. <br> |
| cw | str &#124; None | | CW of note. |
| localOnly | bool | False | True to post locally only. |
| noExtractMentions | bool | False | If True, do not extract mentions from the body. |
| noExtractHashtags | bool | False | If True, do not extract hashtags from the body. |
| noExtractEmojis | bool | False | If set to True, emojis will not be extracted from the text. <br> |
| fileIds | list<br>(str) | | IDs of files to attach. <br> |
| replyId | str &#124; None | | ID of the note to reply to. |
| renoteId | str &#124; None | | ID of the note to renote. |
| channelId | str &#124; None | | ID of the channel to post to. <br> |
| poll | object &#124; None | | Parameters related to voting. |

### type

| Name | Type | Default | Description |
| - | - | - | - |
| choices | list | | choices. |
| multiple | bool | False | True allows multiple selections. <br> |
| expiresAt | int &#124; None | | Voting deadline. Specified in epoch seconds. <br> |
| expiredAfter | int &#124; None | | If specified, voting will end expiredAfter seconds after the note is created. If specified together with expiresAt, expiresAt takes precedence. <br> |

<!--
| Name | Type | Default | Description |
| - | - | - | - |
| | | |
| | | |
| | | |
-->
## notes_delete
Delete notes.

| Name | Type | Default | Description |
| - | - | - | - |
| noteId | str | | Note id. |